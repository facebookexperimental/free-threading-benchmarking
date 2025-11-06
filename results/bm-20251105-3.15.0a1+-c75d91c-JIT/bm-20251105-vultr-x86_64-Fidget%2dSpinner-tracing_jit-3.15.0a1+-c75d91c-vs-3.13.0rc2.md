# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: c75d91c
- commit date: 2025-11-05
- overall geometric mean: 1.061x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.77 sec: 1.06x slower                                                  |
| html5lib       | 67.0 ms                                                      | 67.5 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 560 ms: 1.57x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 601 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 482 ms: 1.32x faster                                                    |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 546 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.1 ms: 1.29x faster                                                   |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                    |
| nbody          | 85.1 ms                                                      | 85.5 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                        | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                   |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                   |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.07 ms: 1.16x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 184 us: 1.14x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 79.1 ms: 1.08x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 55.0 ms: 1.08x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 298 us: 1.01x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| genshi_text     | 21.5 ms                                                      | 22.1 ms: 1.03x slower                                                   |
| django_template | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 56.2 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 21.4 ms: 2.11x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.6 ms: 2.02x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.36 sec: 1.73x faster                                                  |
| async_tree_io              | 876 ms                                                       | 560 ms: 1.57x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 25.3 us: 1.54x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 601 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                    |
| scimark_fft                | 349 ms                                                       | 252 ms: 1.39x faster                                                    |
| scimark_sor                | 134 ms                                                       | 96.9 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                    |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                    |
| spectral_norm              | 111 ms                                                       | 82.9 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 482 ms: 1.32x faster                                                    |
| float                      | 77.5 ms                                                      | 60.1 ms: 1.29x faster                                                   |
| pyflate                    | 449 ms                                                       | 367 ms: 1.22x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                   |
| logging_silent             | 103 ns                                                       | 86.2 ns: 1.19x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.2 ms: 1.18x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.07 ms: 1.16x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 184 us: 1.14x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.23 ms: 1.11x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 2.81 ms: 1.11x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 675 ms: 1.09x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 79.1 ms: 1.08x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.39 sec: 1.08x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 55.0 ms: 1.08x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| chaos                      | 57.3 ms                                                      | 53.2 ms: 1.08x faster                                                   |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.14 sec: 1.07x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 105 ms: 1.07x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                   |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                    |
| logging_simple             | 6.16 us                                                      | 5.93 us: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 66.1 ms: 1.03x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.70 us: 1.02x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                   |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                                    |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                    |
| nbody                      | 85.1 ms                                                      | 85.5 ms: 1.00x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 75.3 ms: 1.01x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 67.5 ms: 1.01x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 298 us: 1.01x slower                                                    |
| generators                 | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.10 ms: 1.02x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 22.1 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.5 ms: 1.03x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 546 ms: 1.05x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.77 sec: 1.06x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 169 ms: 1.09x slower                                                    |
| raytrace                   | 253 ms                                                       | 276 ms: 1.09x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 86.4 ms: 1.10x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                   |
| sympy_expand               | 457 ms                                                       | 510 ms: 1.12x slower                                                    |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                    |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 56.2 ms: 1.15x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.72 ms: 1.50x slower                                                   |
| telco                      | 7.82 ms                                                      | 162 ms: 20.67x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (3): thrift, pylint, json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251105-3.15.0a1+-c75d91c-JIT/bm-20251105-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-c75d91c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x