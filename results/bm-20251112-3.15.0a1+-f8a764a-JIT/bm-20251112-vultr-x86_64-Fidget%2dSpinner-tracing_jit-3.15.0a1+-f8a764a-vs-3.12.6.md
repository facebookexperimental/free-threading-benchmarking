# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f8a764a
- commit date: 2025-11-12
- overall geometric mean: 1.096x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| html5lib       | 63.6 ms                                                | 69.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 561 ms: 1.93x faster                                                    |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.90x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 598 ms: 1.86x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                    |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 59.4 ms: 1.36x faster                                                   |
| nbody          | 89.3 ms                                                | 84.0 ms: 1.06x faster                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                   |
| regex_compile  | 142 ms                                                 | 128 ms: 1.12x faster                                                    |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                    |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.38 ms: 1.10x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 78.9 ms: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 55.6 ms: 1.06x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 295 us: 1.04x faster                                                    |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                   |
| genshi_text     | 22.8 ms                                                | 21.8 ms: 1.05x faster                                                   |
| django_template | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 21.7 ms: 2.12x faster                                                   |
| richards_super             | 51.9 ms                                                | 26.0 ms: 2.00x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 561 ms: 1.93x faster                                                    |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.90x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 598 ms: 1.86x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.81x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.81x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.2 us: 1.54x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                    |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                    |
| float                      | 80.8 ms                                                | 59.4 ms: 1.36x faster                                                   |
| go                         | 139 ms                                                 | 103 ms: 1.35x faster                                                    |
| scimark_fft                | 342 ms                                                 | 254 ms: 1.34x faster                                                    |
| scimark_sor                | 130 ms                                                 | 96.7 ms: 1.34x faster                                                   |
| spectral_norm              | 110 ms                                                 | 82.3 ms: 1.34x faster                                                   |
| logging_silent             | 109 ns                                                 | 86.5 ns: 1.26x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 55.3 ms: 1.24x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.6 us: 1.20x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                    |
| pyflate                    | 448 ms                                                 | 376 ms: 1.19x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.7 ms: 1.17x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                   |
| chaos                      | 62.8 ms                                                | 54.3 ms: 1.16x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.78 us: 1.15x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.14 sec: 1.14x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                   |
| raytrace                   | 299 ms                                                 | 264 ms: 1.13x faster                                                    |
| logging_format             | 7.35 us                                                | 6.50 us: 1.13x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 101 ms: 1.12x faster                                                    |
| generators                 | 32.2 ms                                                | 28.7 ms: 1.12x faster                                                   |
| regex_compile              | 142 ms                                                 | 128 ms: 1.12x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.38 ms: 1.10x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 676 ms: 1.10x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.07 ms: 1.08x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 78.9 ms: 1.08x faster                                                   |
| thrift                     | 791 us                                                 | 738 us: 1.07x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                                    |
| nbody                      | 89.3 ms                                                | 84.0 ms: 1.06x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 55.6 ms: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                  |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.8 ms: 1.05x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 75.5 ms: 1.05x faster                                                   |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 295 us: 1.04x faster                                                    |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                   |
| fannkuch                   | 372 ms                                                 | 374 ms: 1.00x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                   |
| django_template            | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.2 ms: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.63 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 175 ms: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                    |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.08x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.1 ms: 1.09x slower                                                   |
| nqueens                    | 80.1 ms                                                | 87.0 ms: 1.09x slower                                                   |
| sympy_expand               | 468 ms                                                 | 516 ms: 1.10x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                   |
| coverage                   | 71.4 ms                                                | 82.3 ms: 1.15x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.6 ms: 1.17x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.57 ms: 1.32x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.90 ms: 1.74x slower                                                   |
| telco                      | 6.53 ms                                                | 160 ms: 24.46x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (2): pylint, hexiom
Ignored benchmarks (22) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251112-3.15.0a1+-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f8a764a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x