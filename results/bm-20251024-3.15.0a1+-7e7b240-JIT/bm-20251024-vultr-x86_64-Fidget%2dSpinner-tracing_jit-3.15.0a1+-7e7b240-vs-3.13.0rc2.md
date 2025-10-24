# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7e7b240
- commit date: 2025-10-24
- overall geometric mean: 1.049x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.02x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.67 sec: 1.02x slower                                                  |
| html5lib       | 67.0 ms                                                      | 70.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 560 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 596 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                    |
| async_generators           | 377 ms                                                       | 374 ms: 1.01x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 61.9 ms: 1.25x faster                                                   |
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| nbody          | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                   |
| regex_compile  | 132 ms                                                       | 131 ms: 1.01x faster                                                    |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 83.3 ms: 1.14x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 190 us: 1.11x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.55 ms: 1.10x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 55.5 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 80.2 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.04x faster                                                    |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.30 ms: 1.01x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| django_template | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 53.7 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.5 ms: 2.01x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.23 sec: 1.91x faster                                                  |
| richards_super             | 51.6 ms                                                      | 27.3 ms: 1.89x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 23.9 us: 1.63x faster                                                   |
| async_tree_io              | 876 ms                                                       | 560 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 596 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                                    |
| deepcopy                   | 355 us                                                       | 256 us: 1.39x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                    |
| scimark_sor                | 134 ms                                                       | 99.2 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                    |
| scimark_fft                | 349 ms                                                       | 266 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                    |
| spectral_norm              | 111 ms                                                       | 85.4 ms: 1.30x faster                                                   |
| float                      | 77.5 ms                                                      | 61.9 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                   |
| pyflate                    | 449 ms                                                       | 385 ms: 1.16x faster                                                    |
| logging_silent             | 103 ns                                                       | 88.2 ns: 1.16x faster                                                   |
| go                         | 141 ms                                                       | 123 ms: 1.14x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.3 ms: 1.14x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.9 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 190 us: 1.11x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.83 ms: 1.11x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.55 ms: 1.10x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.04 sec: 1.10x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 103 ms: 1.09x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.36 ms: 1.08x faster                                                   |
| comprehensions             | 16.5 us                                                      | 15.3 us: 1.07x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 55.5 ms: 1.07x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 80.2 ms: 1.07x faster                                                   |
| pylint                     | 317 ms                                                       | 300 ms: 1.06x faster                                                    |
| chaos                      | 57.3 ms                                                      | 54.4 ms: 1.05x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 706 ms: 1.04x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.04x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 65.4 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.03x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                   |
| 2to3                       | 260 ms                                                       | 256 ms: 1.02x faster                                                    |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.30 ms: 1.01x faster                                                   |
| regex_compile              | 132 ms                                                       | 131 ms: 1.01x faster                                                    |
| async_generators           | 377 ms                                                       | 374 ms: 1.01x faster                                                    |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 74.3 ms: 1.01x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.7 ms: 1.00x faster                                                   |
| fannkuch                   | 370 ms                                                       | 368 ms: 1.00x faster                                                    |
| docutils                   | 2.62 sec                                                     | 2.67 sec: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.32 us: 1.03x slower                                                   |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                    |
| logging_format             | 6.84 us                                                      | 7.08 us: 1.03x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 162 ms: 1.04x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 70.2 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 20.3 ms: 1.06x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.06x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                   |
| nbody                      | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                   |
| sympy_str                  | 275 ms                                                       | 294 ms: 1.07x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 85.7 ms: 1.09x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 53.7 ms: 1.10x slower                                                   |
| raytrace                   | 253 ms                                                       | 279 ms: 1.11x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                   |
| sympy_expand               | 457 ms                                                       | 509 ms: 1.11x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.33 ms: 1.38x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                   |
| telco                      | 7.82 ms                                                      | 162 ms: 20.73x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                            |

Benchmark hidden because not significant (4): hexiom, generators, genshi_text, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-7e7b240-JIT/bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x