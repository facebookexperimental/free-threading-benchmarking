# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7e2bc1d
- commit date: 2025-11-08
- overall geometric mean: 1.066x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                  |
| html5lib       | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 564 ms: 1.55x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 602 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                                    |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.7 ms: 1.28x faster                                                   |
| pidigits       | 217 ms                                                       | 210 ms: 1.03x faster                                                    |
| nbody          | 85.1 ms                                                      | 83.3 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                   |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 182 us: 1.15x faster                                                    |
| json_dumps           | 10.5 ms                                                      | 9.14 ms: 1.15x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 82.7 ms: 1.15x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 77.9 ms: 1.10x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 54.4 ms: 1.09x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.85 sec: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 297 us: 1.01x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.01x faster                                                   |
| django_template | 34.1 ms                                                      | 34.4 ms: 1.01x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 53.6 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.9 ms: 2.17x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.2 ms: 2.05x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.78x faster                                                  |
| async_tree_io              | 876 ms                                                       | 564 ms: 1.55x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 25.2 us: 1.55x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 602 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| deepcopy                   | 355 us                                                       | 249 us: 1.43x faster                                                    |
| go                         | 141 ms                                                       | 102 ms: 1.37x faster                                                    |
| scimark_sor                | 134 ms                                                       | 98.2 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.35x faster                                                    |
| scimark_fft                | 349 ms                                                       | 260 ms: 1.35x faster                                                    |
| spectral_norm              | 111 ms                                                       | 83.3 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                                    |
| float                      | 77.5 ms                                                      | 60.7 ms: 1.28x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                   |
| pyflate                    | 449 ms                                                       | 377 ms: 1.19x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.2 ms: 1.18x faster                                                   |
| logging_silent             | 103 ns                                                       | 87.2 ns: 1.18x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 182 us: 1.15x faster                                                    |
| json_dumps                 | 10.5 ms                                                      | 9.14 ms: 1.15x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 82.7 ms: 1.15x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.15 ms: 1.14x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 2.79 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.98 sec: 1.12x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 102 ms: 1.10x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 77.9 ms: 1.10x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 54.4 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 679 ms: 1.09x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.85 sec: 1.08x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.38 sec: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                   |
| chaos                      | 57.3 ms                                                      | 53.4 ms: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                    |
| thrift                     | 778 us                                                       | 745 us: 1.04x faster                                                    |
| meteor_contest             | 102 ms                                                       | 97.5 ms: 1.04x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.92 us: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| pidigits                   | 217 ms                                                       | 210 ms: 1.03x faster                                                    |
| logging_format             | 6.84 us                                                      | 6.64 us: 1.03x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 66.3 ms: 1.02x faster                                                   |
| nbody                      | 85.1 ms                                                      | 83.3 ms: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.01x faster                                                   |
| fannkuch                   | 370 ms                                                       | 367 ms: 1.01x faster                                                    |
| hexiom                     | 5.99 ms                                                      | 6.03 ms: 1.01x slower                                                   |
| django_template            | 34.1 ms                                                      | 34.4 ms: 1.01x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 297 us: 1.01x slower                                                    |
| json                       | 4.93 ms                                                      | 5.00 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.01x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                   |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 169 ms: 1.08x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 85.4 ms: 1.09x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 53.6 ms: 1.10x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                   |
| sympy_expand               | 457 ms                                                       | 506 ms: 1.11x slower                                                    |
| sympy_str                  | 275 ms                                                       | 306 ms: 1.11x slower                                                    |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.34 ms: 1.38x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.97 ms: 1.47x slower                                                   |
| telco                      | 7.82 ms                                                      | 162 ms: 20.68x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (5): pylint, pycparser, dulwich_log, sqlite_synth, regex_dna
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251108-3.15.0a1+-7e2bc1d-JIT/bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x