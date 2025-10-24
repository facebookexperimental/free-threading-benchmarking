# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7b2a8ca
- commit date: 2025-10-24
- overall geometric mean: 1.038x faster
- HPT reliability: 99.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                  |
| html5lib       | 67.0 ms                                                      | 71.7 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 320 ms: 1.44x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 635 ms: 1.44x faster                                                    |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                    |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.31x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                    |
| async_generators           | 377 ms                                                       | 367 ms: 1.03x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 63.3 ms: 1.22x faster                                                   |
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| nbody          | 85.1 ms                                                      | 90.1 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                   |
| regex_compile  | 132 ms                                                       | 128 ms: 1.03x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                   |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 183 us: 1.15x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 55.0 ms: 1.08x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 79.4 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                    |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                    |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.30 ms: 1.01x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                   |
| django_template | 34.1 ms                                                      | 36.2 ms: 1.06x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 52.5 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.4 ms: 2.02x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.23 sec: 1.92x faster                                                  |
| richards_super             | 51.6 ms                                                      | 27.2 ms: 1.90x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 23.9 us: 1.64x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 320 ms: 1.44x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 635 ms: 1.44x faster                                                    |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                    |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                    |
| scimark_fft                | 349 ms                                                       | 264 ms: 1.33x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                    |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.31x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                    |
| spectral_norm              | 111 ms                                                       | 85.3 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                    |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.23x faster                                                    |
| float                      | 77.5 ms                                                      | 63.3 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                   |
| pyflate                    | 449 ms                                                       | 379 ms: 1.18x faster                                                    |
| logging_silent             | 103 ns                                                       | 86.7 ns: 1.18x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 183 us: 1.15x faster                                                    |
| go                         | 141 ms                                                       | 125 ms: 1.13x faster                                                    |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 3.99 sec: 1.11x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                   |
| pylint                     | 317 ms                                                       | 289 ms: 1.10x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 59.8 ms: 1.09x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 55.0 ms: 1.08x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 79.4 ms: 1.08x faster                                                   |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.47 ms: 1.05x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 65.0 ms: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                    |
| fannkuch                   | 370 ms                                                       | 355 ms: 1.04x faster                                                    |
| regex_compile              | 132 ms                                                       | 128 ms: 1.03x faster                                                    |
| async_generators           | 377 ms                                                       | 367 ms: 1.03x faster                                                    |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 73.5 ms: 1.02x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                   |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.30 ms: 1.01x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.92 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 4.97 ms: 1.01x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.1 ms: 1.01x slower                                                   |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                    |
| logging_format             | 6.84 us                                                      | 6.92 us: 1.01x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.02x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 115 ms: 1.02x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 20.1 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 90.1 ms: 1.06x slower                                                   |
| django_template            | 34.1 ms                                                      | 36.2 ms: 1.06x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 165 ms: 1.06x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 71.7 ms: 1.07x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 84.5 ms: 1.08x slower                                                   |
| sympy_str                  | 275 ms                                                       | 296 ms: 1.08x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 52.5 ms: 1.08x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                   |
| raytrace                   | 253 ms                                                       | 280 ms: 1.11x slower                                                    |
| sympy_expand               | 457 ms                                                       | 515 ms: 1.13x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.08 ms: 1.30x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.43x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 4.69 ms: 1.50x slower                                                   |
| telco                      | 7.82 ms                                                      | 160 ms: 20.45x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                            |

Benchmark hidden because not significant (4): logging_simple, genshi_text, coverage, chaos
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-7b2a8ca-JIT/bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 99.70% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x