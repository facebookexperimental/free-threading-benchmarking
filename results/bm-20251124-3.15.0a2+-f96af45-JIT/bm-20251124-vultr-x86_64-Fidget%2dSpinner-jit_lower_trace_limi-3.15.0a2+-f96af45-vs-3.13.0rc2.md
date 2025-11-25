# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_lower_trace_limi
- machine: linux-x86_64
- commit hash: f96af45
- commit date: 2025-11-24
- overall geometric mean: 1.056x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                             |
| html5lib       | 67.0 ms                                                      | 68.1 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 571 ms: 1.54x faster                                                             |
| async_tree_io_tg           | 913 ms                                                       | 608 ms: 1.50x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                             |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 517 ms: 1.29x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 516 ms: 1.24x faster                                                             |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                             |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.1 ms: 1.29x faster                                                            |
| pidigits       | 217 ms                                                       | 207 ms: 1.04x faster                                                             |
| Geometric mean | (ref)                                                        | 1.10x faster                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                            |
| regex_dna      | 180 ms                                                       | 167 ms: 1.08x faster                                                             |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                            |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                             |
| Geometric mean | (ref)                                                        | 1.09x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 83.1 ms: 1.14x faster                                                            |
| json_dumps           | 10.5 ms                                                      | 9.34 ms: 1.13x faster                                                            |
| unpickle_pure_python | 210 us                                                       | 189 us: 1.11x faster                                                             |
| xml_etree_process    | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                            |
| tomli_loads          | 2.01 sec                                                     | 1.85 sec: 1.09x faster                                                           |
| xml_etree_generate   | 85.4 ms                                                      | 78.7 ms: 1.09x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                             |
| pickle_pure_python   | 294 us                                                       | 298 us: 1.01x slower                                                             |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                                            |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                            |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                            |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.7 ms: 1.06x faster                                                            |
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                            |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                            |
| genshi_xml      | 48.8 ms                                                      | 55.0 ms: 1.13x slower                                                            |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.2 ms: 2.04x faster                                                            |
| richards_super             | 51.6 ms                                                      | 26.1 ms: 1.98x faster                                                            |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                           |
| deepcopy_memo              | 39.1 us                                                      | 25.3 us: 1.54x faster                                                            |
| async_tree_io              | 876 ms                                                       | 571 ms: 1.54x faster                                                             |
| async_tree_io_tg           | 913 ms                                                       | 608 ms: 1.50x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                             |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                                             |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                             |
| spectral_norm              | 111 ms                                                       | 81.8 ms: 1.36x faster                                                            |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                             |
| scimark_fft                | 349 ms                                                       | 270 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 517 ms: 1.29x faster                                                             |
| float                      | 77.5 ms                                                      | 60.1 ms: 1.29x faster                                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 516 ms: 1.24x faster                                                             |
| scimark_sor                | 134 ms                                                       | 112 ms: 1.20x faster                                                             |
| pyflate                    | 449 ms                                                       | 376 ms: 1.19x faster                                                             |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                            |
| regex_effbot               | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                            |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.12 ms: 1.14x faster                                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.2 ms: 1.14x faster                                                            |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.1 ms: 1.14x faster                                                            |
| json_dumps                 | 10.5 ms                                                      | 9.34 ms: 1.13x faster                                                            |
| unpickle_pure_python       | 210 us                                                       | 189 us: 1.11x faster                                                             |
| bpe_tokeniser              | 4.45 sec                                                     | 4.03 sec: 1.10x faster                                                           |
| xml_etree_process          | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                            |
| tomli_loads                | 2.01 sec                                                     | 1.85 sec: 1.09x faster                                                           |
| xml_etree_generate         | 85.4 ms                                                      | 78.7 ms: 1.09x faster                                                            |
| scimark_lu                 | 113 ms                                                       | 104 ms: 1.09x faster                                                             |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                            |
| regex_dna                  | 180 ms                                                       | 167 ms: 1.08x faster                                                             |
| logging_silent             | 103 ns                                                       | 95.3 ns: 1.08x faster                                                            |
| pprint_safe_repr           | 738 ms                                                       | 688 ms: 1.07x faster                                                             |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                            |
| mako                       | 11.3 ms                                                      | 10.7 ms: 1.06x faster                                                            |
| deltablue                  | 3.12 ms                                                      | 2.95 ms: 1.06x faster                                                            |
| logging_simple             | 6.16 us                                                      | 5.83 us: 1.06x faster                                                            |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                             |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.05x faster                                                           |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                             |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                             |
| pidigits                   | 217 ms                                                       | 207 ms: 1.04x faster                                                             |
| logging_format             | 6.84 us                                                      | 6.57 us: 1.04x faster                                                            |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                             |
| meteor_contest             | 102 ms                                                       | 98.0 ms: 1.04x faster                                                            |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                            |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                            |
| coverage                   | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                            |
| thrift                     | 778 us                                                       | 763 us: 1.02x faster                                                             |
| fannkuch                   | 370 ms                                                       | 364 ms: 1.02x faster                                                             |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.02x faster                                                            |
| python_startup_no_site     | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                            |
| dulwich_log                | 74.8 ms                                                      | 73.8 ms: 1.01x faster                                                            |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                            |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                            |
| pickle_pure_python         | 294 us                                                       | 298 us: 1.01x slower                                                             |
| html5lib                   | 67.0 ms                                                      | 68.1 ms: 1.02x slower                                                            |
| hexiom                     | 5.99 ms                                                      | 6.12 ms: 1.02x slower                                                            |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                             |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                            |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                             |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                                            |
| sympy_integrate            | 19.8 ms                                                      | 21.2 ms: 1.07x slower                                                            |
| nqueens                    | 78.6 ms                                                      | 85.1 ms: 1.08x slower                                                            |
| raytrace                   | 253 ms                                                       | 278 ms: 1.10x slower                                                             |
| sympy_sum                  | 156 ms                                                       | 173 ms: 1.12x slower                                                             |
| sympy_expand               | 457 ms                                                       | 512 ms: 1.12x slower                                                             |
| genshi_xml                 | 48.8 ms                                                      | 55.0 ms: 1.13x slower                                                            |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                            |
| sympy_str                  | 275 ms                                                       | 313 ms: 1.14x slower                                                             |
| bench_thread_pool          | 919 us                                                       | 1.09 ms: 1.19x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 13.1 ms: 1.19x slower                                                            |
| gc_traversal               | 3.14 ms                                                      | 4.47 ms: 1.42x slower                                                            |
| create_gc_cycles           | 1.34 ms                                                      | 1.96 ms: 1.47x slower                                                            |
| telco                      | 7.82 ms                                                      | 160 ms: 20.39x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                     |

Benchmark hidden because not significant (5): pylint, pycparser, nbody, sqlite_synth, generators
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251124-3.15.0a2+-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.056x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x