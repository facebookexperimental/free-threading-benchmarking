# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: e4f1624
- commit date: 2025-10-21
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| html5lib       | 67.0 ms                                                      | 63.8 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 306 ms: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                                    |
| async_tree_io              | 876 ms                                                       | 592 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 474 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                    |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                                    |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 62.7 ms: 1.24x faster                                                   |
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| nbody          | 85.1 ms                                                      | 97.2 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                   |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                    |
| regex_compile  | 132 ms                                                       | 139 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 8.94 ms: 1.18x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 52.2 ms: 1.14x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 185 us: 1.14x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 76.1 ms: 1.12x faster                                                   |
| json_loads           | 27.0 us                                                      | 25.7 us: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.9 ms: 1.01x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 299 us: 1.02x slower                                                    |
| xml_etree_parse      | 136 ms                                                       | 144 ms: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                   |
| python_startup         | 11.0 ms                                                      | 12.8 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.7 ms: 1.09x faster                                                   |
| mako            | 11.3 ms                                                      | 11.0 ms: 1.03x faster                                                   |
| django_template | 34.1 ms                                                      | 34.4 ms: 1.01x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 49.4 ms: 1.01x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.4 ms: 2.02x faster                                                   |
| richards_super             | 51.6 ms                                                      | 26.5 ms: 1.95x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 21.8 us: 1.79x faster                                                   |
| deepcopy                   | 355 us                                                       | 227 us: 1.57x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 306 ms: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                                    |
| async_tree_io              | 876 ms                                                       | 592 ms: 1.48x faster                                                    |
| scimark_fft                | 349 ms                                                       | 242 ms: 1.44x faster                                                    |
| mdp                        | 2.36 sec                                                     | 1.63 sec: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 474 ms: 1.41x faster                                                    |
| scimark_sor                | 134 ms                                                       | 97.5 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                    |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                    |
| logging_silent             | 103 ns                                                       | 76.1 ns: 1.35x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.35 us: 1.32x faster                                                   |
| spectral_norm              | 111 ms                                                       | 84.4 ms: 1.32x faster                                                   |
| float                      | 77.5 ms                                                      | 62.7 ms: 1.24x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.84 ms: 1.23x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 94.5 ms: 1.19x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 54.9 ms: 1.19x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 8.94 ms: 1.18x faster                                                   |
| go                         | 141 ms                                                       | 121 ms: 1.17x faster                                                    |
| pyflate                    | 449 ms                                                       | 394 ms: 1.14x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 52.2 ms: 1.14x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 185 us: 1.14x faster                                                    |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.76 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 76.1 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.96 sec: 1.12x faster                                                  |
| comprehensions             | 16.5 us                                                      | 14.7 us: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 662 ms: 1.11x faster                                                    |
| coverage                   | 83.0 ms                                                      | 75.1 ms: 1.10x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.36 sec: 1.10x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 19.7 ms: 1.09x faster                                                   |
| chaos                      | 57.3 ms                                                      | 52.9 ms: 1.08x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.7 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 146 us: 1.06x faster                                                    |
| thrift                     | 778 us                                                       | 740 us: 1.05x faster                                                    |
| json_loads                 | 27.0 us                                                      | 25.7 us: 1.05x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 63.8 ms: 1.05x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.87 us: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| fannkuch                   | 370 ms                                                       | 357 ms: 1.04x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.13 us: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.61 us: 1.04x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.03x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 65.7 ms: 1.03x faster                                                   |
| mako                       | 11.3 ms                                                      | 11.0 ms: 1.03x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                   |
| json                       | 4.93 ms                                                      | 4.81 ms: 1.02x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.90 ms: 1.02x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 73.9 ms: 1.01x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.9 ms: 1.01x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                   |
| django_template            | 34.1 ms                                                      | 34.4 ms: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.4 ms: 1.01x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 19.5 ms: 1.01x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 299 us: 1.02x slower                                                    |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 80.9 ms: 1.03x slower                                                   |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                    |
| sympy_expand               | 457 ms                                                       | 473 ms: 1.04x slower                                                    |
| meteor_contest             | 102 ms                                                       | 106 ms: 1.04x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 965 us: 1.05x slower                                                    |
| regex_compile              | 132 ms                                                       | 139 ms: 1.05x slower                                                    |
| xml_etree_parse            | 136 ms                                                       | 144 ms: 1.05x slower                                                    |
| raytrace                   | 253 ms                                                       | 268 ms: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.21 sec: 1.08x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                   |
| nbody                      | 85.1 ms                                                      | 97.2 ms: 1.14x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.8 ms: 1.17x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.36x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 2.02 ms: 1.51x slower                                                   |
| telco                      | 7.82 ms                                                      | 157 ms: 20.02x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                            |

Benchmark hidden because not significant (3): sympy_sum, docutils, regex_effbot
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251021-3.15.0a1+-e4f1624-CLANG,JIT/bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.20x