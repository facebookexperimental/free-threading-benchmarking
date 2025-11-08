# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f547880
- commit date: 2025-11-08
- overall geometric mean: 1.064x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.04x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.79 sec: 1.07x slower                                                  |
| html5lib       | 67.0 ms                                                      | 68.0 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 563 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 598 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                    |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                    |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 25.0 ms: 1.06x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                   |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                    |
| nbody          | 85.1 ms                                                      | 86.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                        | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                   |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                    |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.03 ms: 1.17x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 184 us: 1.14x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 77.8 ms: 1.10x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 300 us: 1.02x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.26 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                   |
| django_template | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 55.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 21.8 ms: 2.08x faster                                                   |
| richards_super             | 51.6 ms                                                      | 26.1 ms: 1.98x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.35 sec: 1.75x faster                                                  |
| async_tree_io              | 876 ms                                                       | 563 ms: 1.56x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 25.2 us: 1.55x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 598 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                    |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                    |
| deepcopy                   | 355 us                                                       | 255 us: 1.40x faster                                                    |
| scimark_sor                | 134 ms                                                       | 96.6 ms: 1.39x faster                                                   |
| scimark_fft                | 349 ms                                                       | 253 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                    |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                                    |
| spectral_norm              | 111 ms                                                       | 82.7 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                    |
| float                      | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                   |
| pyflate                    | 449 ms                                                       | 369 ms: 1.21x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 54.9 ms: 1.19x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                   |
| logging_silent             | 103 ns                                                       | 87.8 ns: 1.17x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.03 ms: 1.17x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.04 ms: 1.17x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 184 us: 1.14x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.97 sec: 1.12x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 101 ms: 1.11x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.82 ms: 1.11x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 77.8 ms: 1.10x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 688 ms: 1.07x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                    |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.05x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.4 ms: 1.05x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                    |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                    |
| meteor_contest             | 102 ms                                                       | 97.2 ms: 1.05x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.90 us: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.56 us: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 251 ms: 1.04x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 65.7 ms: 1.03x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                   |
| thrift                     | 778 us                                                       | 763 us: 1.02x faster                                                    |
| fannkuch                   | 370 ms                                                       | 363 ms: 1.02x faster                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.26 ms: 1.02x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 75.9 ms: 1.01x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 68.0 ms: 1.02x slower                                                   |
| nbody                      | 85.1 ms                                                      | 86.5 ms: 1.02x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 300 us: 1.02x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 6.12 ms: 1.02x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.02x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.9 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 25.0 ms: 1.06x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.79 sec: 1.07x slower                                                  |
| raytrace                   | 253 ms                                                       | 275 ms: 1.09x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 85.4 ms: 1.09x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 170 ms: 1.09x slower                                                    |
| sympy_expand               | 457 ms                                                       | 503 ms: 1.10x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                   |
| sympy_str                  | 275 ms                                                       | 307 ms: 1.12x slower                                                    |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 55.5 ms: 1.14x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.39 ms: 1.40x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.90 ms: 1.42x slower                                                   |
| telco                      | 7.82 ms                                                      | 160 ms: 20.42x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (4): pylint, pycparser, json, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251108-3.15.0a1+-f547880-JIT/bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.064x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x