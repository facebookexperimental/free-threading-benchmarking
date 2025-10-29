# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: 7be738d
- commit date: 2025-10-28
- overall geometric mean: 1.067x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 564 ms: 1.55x faster                                                             |
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                             |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                             |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                             |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                            |
| nbody          | 85.1 ms                                                      | 73.5 ms: 1.16x faster                                                            |
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                             |
| Geometric mean | (ref)                                                        | 1.18x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.55 ms: 1.21x faster                                                            |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                             |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                             |
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                        | 1.09x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 184 us: 1.14x faster                                                             |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.7 ms: 1.13x faster                                                            |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                           |
| json_dumps           | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                            |
| xml_etree_process    | 59.3 ms                                                      | 55.4 ms: 1.07x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                             |
| xml_etree_generate   | 85.4 ms                                                      | 81.0 ms: 1.05x faster                                                            |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                                     |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                            |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                            |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                            |
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                            |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                            |
| genshi_xml      | 48.8 ms                                                      | 54.0 ms: 1.11x slower                                                            |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.0 ms: 2.26x faster                                                            |
| richards_super             | 51.6 ms                                                      | 24.0 ms: 2.15x faster                                                            |
| mdp                        | 2.36 sec                                                     | 1.35 sec: 1.75x faster                                                           |
| deepcopy_memo              | 39.1 us                                                      | 23.7 us: 1.65x faster                                                            |
| async_tree_io              | 876 ms                                                       | 564 ms: 1.55x faster                                                             |
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                             |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                             |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                             |
| scimark_sor                | 134 ms                                                       | 97.2 ms: 1.38x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                             |
| scimark_fft                | 349 ms                                                       | 261 ms: 1.34x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                             |
| float                      | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                            |
| spectral_norm              | 111 ms                                                       | 87.0 ms: 1.28x faster                                                            |
| go                         | 141 ms                                                       | 115 ms: 1.23x faster                                                             |
| regex_effbot               | 3.08 ms                                                      | 2.55 ms: 1.21x faster                                                            |
| logging_silent             | 103 ns                                                       | 86.7 ns: 1.18x faster                                                            |
| pyflate                    | 449 ms                                                       | 381 ms: 1.18x faster                                                             |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 56.5 ms: 1.16x faster                                                            |
| nbody                      | 85.1 ms                                                      | 73.5 ms: 1.16x faster                                                            |
| unpickle_pure_python       | 210 us                                                       | 184 us: 1.14x faster                                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.7 ms: 1.13x faster                                                            |
| deltablue                  | 3.12 ms                                                      | 2.78 ms: 1.12x faster                                                            |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                             |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                           |
| json_dumps                 | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                            |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.27 ms: 1.10x faster                                                            |
| bpe_tokeniser              | 4.45 sec                                                     | 4.05 sec: 1.10x faster                                                           |
| scimark_lu                 | 113 ms                                                       | 103 ms: 1.09x faster                                                             |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                            |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                             |
| xml_etree_process          | 59.3 ms                                                      | 55.4 ms: 1.07x faster                                                            |
| logging_simple             | 6.16 us                                                      | 5.77 us: 1.07x faster                                                            |
| chaos                      | 57.3 ms                                                      | 53.7 ms: 1.07x faster                                                            |
| logging_format             | 6.84 us                                                      | 6.45 us: 1.06x faster                                                            |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                             |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                             |
| xml_etree_generate         | 85.4 ms                                                      | 81.0 ms: 1.05x faster                                                            |
| mako                       | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                            |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                           |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                             |
| dulwich_log                | 74.8 ms                                                      | 72.3 ms: 1.03x faster                                                            |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                            |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                             |
| fannkuch                   | 370 ms                                                       | 363 ms: 1.02x faster                                                             |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.02x faster                                                            |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                            |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                             |
| crypto_pyaes               | 67.9 ms                                                      | 67.0 ms: 1.01x faster                                                            |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                            |
| thrift                     | 778 us                                                       | 771 us: 1.01x faster                                                             |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                            |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                             |
| json                       | 4.93 ms                                                      | 4.89 ms: 1.01x faster                                                            |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                            |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                           |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                            |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.03x slower                                                            |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.03x slower                                                             |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                            |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                             |
| hexiom                     | 5.99 ms                                                      | 6.38 ms: 1.06x slower                                                            |
| raytrace                   | 253 ms                                                       | 269 ms: 1.07x slower                                                             |
| sympy_sum                  | 156 ms                                                       | 169 ms: 1.09x slower                                                             |
| sympy_expand               | 457 ms                                                       | 504 ms: 1.10x slower                                                             |
| genshi_xml                 | 48.8 ms                                                      | 54.0 ms: 1.11x slower                                                            |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                            |
| nqueens                    | 78.6 ms                                                      | 87.6 ms: 1.12x slower                                                            |
| sympy_str                  | 275 ms                                                       | 307 ms: 1.12x slower                                                             |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                            |
| gc_traversal               | 3.14 ms                                                      | 4.35 ms: 1.38x slower                                                            |
| create_gc_cycles           | 1.34 ms                                                      | 1.96 ms: 1.47x slower                                                            |
| telco                      | 7.82 ms                                                      | 160 ms: 20.47x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                     |

Benchmark hidden because not significant (4): comprehensions, coverage, html5lib, pickle_pure_python
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, pylint, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (9) of results/bm-20251028-3.15.0a1+-7be738d-JIT/bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d.json: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x