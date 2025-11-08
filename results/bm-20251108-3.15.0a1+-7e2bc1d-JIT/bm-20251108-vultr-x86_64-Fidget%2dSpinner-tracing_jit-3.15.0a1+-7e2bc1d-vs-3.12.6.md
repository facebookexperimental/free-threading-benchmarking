# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7e2bc1d
- commit date: 2025-11-08
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                  |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                    |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 602 ms: 1.84x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                    |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.7 ms: 1.33x faster                                                   |
| nbody          | 89.3 ms                                                | 83.3 ms: 1.07x faster                                                   |
| pidigits       | 184 ms                                                 | 210 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                   |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                    |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                   |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 182 us: 1.21x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 82.7 ms: 1.17x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.14 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 77.9 ms: 1.09x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 54.4 ms: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 297 us: 1.03x faster                                                    |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.2 ms: 1.07x faster                                                   |
| mako            | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                   |
| django_template | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.9 ms: 2.20x faster                                                   |
| richards_super             | 51.9 ms                                                | 25.2 ms: 2.06x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                    |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 602 ms: 1.84x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 25.2 us: 1.60x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                    |
| deepcopy                   | 352 us                                                 | 249 us: 1.41x faster                                                    |
| go                         | 139 ms                                                 | 102 ms: 1.36x faster                                                    |
| float                      | 80.8 ms                                                | 60.7 ms: 1.33x faster                                                   |
| spectral_norm              | 110 ms                                                 | 83.3 ms: 1.32x faster                                                   |
| scimark_sor                | 130 ms                                                 | 98.2 ms: 1.32x faster                                                   |
| scimark_fft                | 342 ms                                                 | 260 ms: 1.32x faster                                                    |
| logging_silent             | 109 ns                                                 | 87.2 ns: 1.25x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 55.2 ms: 1.24x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.79 ms: 1.24x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 182 us: 1.21x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 3.98 sec: 1.19x faster                                                  |
| pyflate                    | 448 ms                                                 | 377 ms: 1.19x faster                                                    |
| chaos                      | 62.8 ms                                                | 53.4 ms: 1.18x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 82.7 ms: 1.17x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                   |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                   |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.14 ms: 1.13x faster                                                   |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                                    |
| logging_simple             | 6.63 us                                                | 5.92 us: 1.12x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 102 ms: 1.12x faster                                                    |
| logging_format             | 7.35 us                                                | 6.64 us: 1.11x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.38 sec: 1.10x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 77.9 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 679 ms: 1.09x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 54.4 ms: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.07x faster                                                   |
| nbody                      | 89.3 ms                                                | 83.3 ms: 1.07x faster                                                   |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                    |
| thrift                     | 791 us                                                 | 745 us: 1.06x faster                                                    |
| meteor_contest             | 104 ms                                                 | 97.5 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.15 ms: 1.06x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 74.7 ms: 1.06x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 297 us: 1.03x faster                                                    |
| hexiom                     | 6.17 ms                                                | 6.03 ms: 1.02x faster                                                   |
| mako                       | 11.0 ms                                                | 10.8 ms: 1.02x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 20.2 ms: 1.02x faster                                                   |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.02x faster                                                    |
| django_template            | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 169 ms: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                  |
| sympy_str                  | 292 ms                                                 | 306 ms: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                   |
| nqueens                    | 80.1 ms                                                | 85.4 ms: 1.07x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                   |
| sympy_expand               | 468 ms                                                 | 506 ms: 1.08x slower                                                    |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                   |
| pidigits                   | 184 ms                                                 | 210 ms: 1.14x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.34 ms: 1.26x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.97 ms: 1.80x slower                                                   |
| telco                      | 6.53 ms                                                | 162 ms: 24.79x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                            |

Benchmark hidden because not significant (3): pylint, json, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251108-3.15.0a1+-7e2bc1d-JIT/bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x