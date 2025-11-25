# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_lower_trace_limi
- machine: linux-x86_64
- commit hash: f96af45
- commit date: 2025-11-24
- overall geometric mean: 1.093x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                             |
| html5lib       | 63.6 ms                                                | 68.1 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 571 ms: 1.90x faster                                                             |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 517 ms: 1.38x faster                                                             |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                             |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.02x slower                                                            |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.1 ms: 1.34x faster                                                            |
| nbody          | 89.3 ms                                                | 85.2 ms: 1.05x faster                                                            |
| pidigits       | 184 ms                                                 | 207 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                            |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                             |
| regex_dna      | 168 ms                                                 | 167 ms: 1.00x faster                                                             |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                  | 1.07x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 189 us: 1.17x faster                                                             |
| xml_etree_iterparse  | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                            |
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                           |
| json_dumps           | 10.4 ms                                                | 9.34 ms: 1.11x faster                                                            |
| xml_etree_process    | 59.0 ms                                                | 54.3 ms: 1.09x faster                                                            |
| xml_etree_generate   | 85.2 ms                                                | 78.7 ms: 1.08x faster                                                            |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                             |
| pickle_pure_python   | 308 us                                                 | 298 us: 1.03x faster                                                             |
| json_loads           | 26.5 us                                                | 28.8 us: 1.08x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                            |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                            |
| mako            | 11.0 ms                                                | 10.7 ms: 1.03x faster                                                            |
| django_template | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                            |
| genshi_xml      | 50.2 ms                                                | 55.0 ms: 1.10x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 22.2 ms: 2.07x faster                                                            |
| richards_super             | 51.9 ms                                                | 26.1 ms: 1.99x faster                                                            |
| async_tree_io              | 1.08 sec                                               | 571 ms: 1.90x faster                                                             |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                             |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                             |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                             |
| deepcopy_memo              | 40.3 us                                                | 25.3 us: 1.59x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 517 ms: 1.38x faster                                                             |
| deepcopy                   | 352 us                                                 | 254 us: 1.38x faster                                                             |
| spectral_norm              | 110 ms                                                 | 81.8 ms: 1.35x faster                                                            |
| float                      | 80.8 ms                                                | 60.1 ms: 1.34x faster                                                            |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                             |
| scimark_fft                | 342 ms                                                 | 270 ms: 1.27x faster                                                             |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                            |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.21x faster                                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 57.2 ms: 1.20x faster                                                            |
| pyflate                    | 448 ms                                                 | 376 ms: 1.19x faster                                                             |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.18x faster                                                           |
| deltablue                  | 3.45 ms                                                | 2.95 ms: 1.17x faster                                                            |
| unpickle_pure_python       | 221 us                                                 | 189 us: 1.17x faster                                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                            |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                             |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.15x faster                                                            |
| logging_silent             | 109 ns                                                 | 95.3 ns: 1.14x faster                                                            |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                           |
| logging_simple             | 6.63 us                                                | 5.83 us: 1.14x faster                                                            |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                             |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                            |
| logging_format             | 7.35 us                                                | 6.57 us: 1.12x faster                                                            |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                            |
| json_dumps                 | 10.4 ms                                                | 9.34 ms: 1.11x faster                                                            |
| scimark_lu                 | 114 ms                                                 | 104 ms: 1.10x faster                                                             |
| xml_etree_process          | 59.0 ms                                                | 54.3 ms: 1.09x faster                                                            |
| xml_etree_generate         | 85.2 ms                                                | 78.7 ms: 1.08x faster                                                            |
| pprint_safe_repr           | 743 ms                                                 | 688 ms: 1.08x faster                                                             |
| raytrace                   | 299 ms                                                 | 278 ms: 1.08x faster                                                             |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                             |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                            |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                           |
| dulwich_log                | 78.9 ms                                                | 73.8 ms: 1.07x faster                                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.12 ms: 1.07x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                             |
| meteor_contest             | 104 ms                                                 | 98.0 ms: 1.06x faster                                                            |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                             |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                           |
| nbody                      | 89.3 ms                                                | 85.2 ms: 1.05x faster                                                            |
| thrift                     | 791 us                                                 | 763 us: 1.04x faster                                                             |
| pickle_pure_python         | 308 us                                                 | 298 us: 1.03x faster                                                             |
| mako                       | 11.0 ms                                                | 10.7 ms: 1.03x faster                                                            |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                             |
| fannkuch                   | 372 ms                                                 | 364 ms: 1.02x faster                                                             |
| hexiom                     | 6.17 ms                                                | 6.12 ms: 1.01x faster                                                            |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                            |
| regex_dna                  | 168 ms                                                 | 167 ms: 1.00x faster                                                             |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.02x slower                                                            |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                            |
| python_startup_no_site     | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                            |
| sympy_integrate            | 20.5 ms                                                | 21.2 ms: 1.03x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                            |
| sympy_sum                  | 166 ms                                                 | 173 ms: 1.05x slower                                                             |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                             |
| nqueens                    | 80.1 ms                                                | 85.1 ms: 1.06x slower                                                            |
| html5lib                   | 63.6 ms                                                | 68.1 ms: 1.07x slower                                                            |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.08x slower                                                             |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.08x slower                                                            |
| sympy_expand               | 468 ms                                                 | 512 ms: 1.10x slower                                                             |
| genshi_xml                 | 50.2 ms                                                | 55.0 ms: 1.10x slower                                                            |
| pidigits                   | 184 ms                                                 | 207 ms: 1.13x slower                                                             |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                            |
| bench_thread_pool          | 941 us                                                 | 1.09 ms: 1.16x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 13.1 ms: 1.21x slower                                                            |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                            |
| gc_traversal               | 3.46 ms                                                | 4.47 ms: 1.29x slower                                                            |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.80x slower                                                            |
| telco                      | 6.53 ms                                                | 160 ms: 24.44x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                                     |

Benchmark hidden because not significant (2): pylint, sqlite_synth
Ignored benchmarks (22) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251124-3.15.0a2+-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x