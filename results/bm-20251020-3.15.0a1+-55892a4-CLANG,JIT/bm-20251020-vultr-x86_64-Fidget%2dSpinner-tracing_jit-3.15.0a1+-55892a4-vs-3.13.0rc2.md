# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 55892a4
- commit date: 2025-10-20
- overall geometric mean: 1.072x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 248 ms: 1.05x faster                                                    |
| html5lib       | 67.0 ms                                                      | 64.3 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_io              | 876 ms                                                       | 599 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 477 ms: 1.40x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| async_tree_none            | 354 ms                                                       | 261 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 477 ms: 1.34x faster                                                    |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 62.5 ms: 1.24x faster                                                   |
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| nbody          | 85.1 ms                                                      | 92.0 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                   |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                   |
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                        | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 8.74 ms: 1.21x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 185 us: 1.13x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 52.7 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 77.2 ms: 1.11x faster                                                   |
| json_loads           | 27.0 us                                                      | 26.1 us: 1.03x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.02 sec: 1.01x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 298 us: 1.01x slower                                                    |
| xml_etree_parse      | 136 ms                                                       | 144 ms: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                   |
| python_startup         | 11.0 ms                                                      | 12.8 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 19.7 ms: 1.10x faster                                                   |
| mako           | 11.3 ms                                                      | 11.4 ms: 1.01x slower                                                   |
| genshi_xml     | 48.8 ms                                                      | 51.6 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.18 sec: 2.00x faster                                                  |
| richards                   | 45.2 ms                                                      | 24.2 ms: 1.87x faster                                                   |
| richards_super             | 51.6 ms                                                      | 28.8 ms: 1.80x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 22.0 us: 1.78x faster                                                   |
| deepcopy                   | 355 us                                                       | 235 us: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_io              | 876 ms                                                       | 599 ms: 1.46x faster                                                    |
| scimark_fft                | 349 ms                                                       | 242 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 477 ms: 1.40x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| async_tree_none            | 354 ms                                                       | 261 ms: 1.36x faster                                                    |
| scimark_sor                | 134 ms                                                       | 99.7 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 477 ms: 1.34x faster                                                    |
| spectral_norm              | 111 ms                                                       | 84.1 ms: 1.32x faster                                                   |
| logging_silent             | 103 ns                                                       | 78.0 ns: 1.31x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.46 us: 1.27x faster                                                   |
| float                      | 77.5 ms                                                      | 62.5 ms: 1.24x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.82 ms: 1.23x faster                                                   |
| go                         | 141 ms                                                       | 116 ms: 1.22x faster                                                    |
| json_dumps                 | 10.5 ms                                                      | 8.74 ms: 1.21x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 94.7 ms: 1.19x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.0 ms: 1.15x faster                                                   |
| pyflate                    | 449 ms                                                       | 395 ms: 1.14x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 185 us: 1.13x faster                                                    |
| comprehensions             | 16.5 us                                                      | 14.6 us: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 52.7 ms: 1.13x faster                                                   |
| pylint                     | 317 ms                                                       | 282 ms: 1.13x faster                                                    |
| coverage                   | 83.0 ms                                                      | 74.1 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.79 ms: 1.12x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 77.2 ms: 1.11x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.03 sec: 1.10x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 19.7 ms: 1.10x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 677 ms: 1.09x faster                                                    |
| chaos                      | 57.3 ms                                                      | 52.7 ms: 1.09x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                   |
| thrift                     | 778 us                                                       | 737 us: 1.06x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 248 ms: 1.05x faster                                                    |
| typing_runtime_protocols   | 155 us                                                       | 148 us: 1.04x faster                                                    |
| html5lib                   | 67.0 ms                                                      | 64.3 ms: 1.04x faster                                                   |
| fannkuch                   | 370 ms                                                       | 356 ms: 1.04x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.13 us: 1.04x faster                                                   |
| generators                 | 28.8 ms                                                      | 27.8 ms: 1.04x faster                                                   |
| json_loads                 | 27.0 us                                                      | 26.1 us: 1.03x faster                                                   |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                   |
| regex_compile              | 132 ms                                                       | 129 ms: 1.03x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 66.6 ms: 1.02x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.91 ms: 1.01x faster                                                   |
| json                       | 4.93 ms                                                      | 4.89 ms: 1.01x faster                                                   |
| mako                       | 11.3 ms                                                      | 11.4 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.02 sec: 1.01x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.4 ms: 1.01x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 298 us: 1.01x slower                                                    |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 80.6 ms: 1.03x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                  |
| meteor_contest             | 102 ms                                                       | 106 ms: 1.04x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| sympy_expand               | 457 ms                                                       | 479 ms: 1.05x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 968 us: 1.05x slower                                                    |
| raytrace                   | 253 ms                                                       | 266 ms: 1.05x slower                                                    |
| xml_etree_parse            | 136 ms                                                       | 144 ms: 1.06x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 51.6 ms: 1.06x slower                                                   |
| nbody                      | 85.1 ms                                                      | 92.0 ms: 1.08x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.12x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.8 ms: 1.16x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.48 ms: 1.43x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 2.03 ms: 1.52x slower                                                   |
| telco                      | 7.82 ms                                                      | 154 ms: 19.71x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                            |

Benchmark hidden because not significant (7): logging_simple, django_template, xml_etree_iterparse, docutils, sympy_sum, logging_format, pathlib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251020-3.15.0a1+-55892a4-CLANG,JIT/bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.21x