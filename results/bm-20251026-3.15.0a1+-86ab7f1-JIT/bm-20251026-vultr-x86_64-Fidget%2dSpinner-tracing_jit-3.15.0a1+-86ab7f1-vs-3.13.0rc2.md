# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 86ab7f1
- commit date: 2025-10-26
- overall geometric mean: 1.057x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.68 sec: 1.03x slower                                                  |
| html5lib       | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 568 ms: 1.54x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 317 ms: 1.46x faster                                                    |
| async_tree_none            | 354 ms                                                       | 250 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                    |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 61.7 ms: 1.26x faster                                                   |
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                    |
| nbody          | 85.1 ms                                                      | 87.7 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                        | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                   |
| regex_compile  | 132 ms                                                       | 129 ms: 1.02x faster                                                    |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                        | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 83.0 ms: 1.14x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 9.21 ms: 1.14x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 185 us: 1.14x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.77 sec: 1.13x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 56.0 ms: 1.06x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 301 us: 1.02x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                   |
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                   |
| genshi_xml      | 48.8 ms                                                      | 53.5 ms: 1.10x slower                                                   |
| django_template | 34.1 ms                                                      | 38.1 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.8 ms: 2.18x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.6 ms: 2.02x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.23 sec: 1.91x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 23.7 us: 1.65x faster                                                   |
| async_tree_io              | 876 ms                                                       | 568 ms: 1.54x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 317 ms: 1.46x faster                                                    |
| async_tree_none            | 354 ms                                                       | 250 ms: 1.41x faster                                                    |
| deepcopy                   | 355 us                                                       | 257 us: 1.38x faster                                                    |
| scimark_sor                | 134 ms                                                       | 98.5 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                    |
| scimark_fft                | 349 ms                                                       | 259 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                    |
| spectral_norm              | 111 ms                                                       | 83.4 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                    |
| float                      | 77.5 ms                                                      | 61.7 ms: 1.26x faster                                                   |
| go                         | 141 ms                                                       | 117 ms: 1.21x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                   |
| logging_silent             | 103 ns                                                       | 86.0 ns: 1.19x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.0 ms: 1.14x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.21 ms: 1.14x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.2 ms: 1.14x faster                                                   |
| pyflate                    | 449 ms                                                       | 394 ms: 1.14x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 185 us: 1.14x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.77 sec: 1.13x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.82 ms: 1.11x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.03 sec: 1.10x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 102 ms: 1.10x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 684 ms: 1.08x faster                                                    |
| comprehensions             | 16.5 us                                                      | 15.3 us: 1.07x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.41 ms: 1.07x faster                                                   |
| pylint                     | 317 ms                                                       | 298 ms: 1.06x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 56.0 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| chaos                      | 57.3 ms                                                      | 54.4 ms: 1.05x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 72.9 ms: 1.03x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                   |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| regex_compile              | 132 ms                                                       | 129 ms: 1.02x faster                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                    |
| coverage                   | 83.0 ms                                                      | 81.9 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                    |
| sympy_integrate            | 19.8 ms                                                      | 19.6 ms: 1.01x faster                                                   |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 6.03 ms: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 5.00 ms: 1.01x slower                                                   |
| thrift                     | 778 us                                                       | 792 us: 1.02x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 301 us: 1.02x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                    |
| logging_format             | 6.84 us                                                      | 7.01 us: 1.02x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.68 sec: 1.03x slower                                                  |
| nbody                      | 85.1 ms                                                      | 87.7 ms: 1.03x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.04x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 162 ms: 1.04x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 81.9 ms: 1.04x slower                                                   |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                   |
| sympy_str                  | 275 ms                                                       | 290 ms: 1.05x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 20.3 ms: 1.06x slower                                                   |
| sympy_expand               | 457 ms                                                       | 496 ms: 1.09x slower                                                    |
| raytrace                   | 253 ms                                                       | 277 ms: 1.10x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 53.5 ms: 1.10x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                   |
| django_template            | 34.1 ms                                                      | 38.1 ms: 1.12x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.06 ms: 1.29x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                   |
| telco                      | 7.82 ms                                                      | 163 ms: 20.85x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                            |

Benchmark hidden because not significant (4): crypto_pyaes, generators, logging_simple, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251026-3.15.0a1+-86ab7f1-JIT/bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x