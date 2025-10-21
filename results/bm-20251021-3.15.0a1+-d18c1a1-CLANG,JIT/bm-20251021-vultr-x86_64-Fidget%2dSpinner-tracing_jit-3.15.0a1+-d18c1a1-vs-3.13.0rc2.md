# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: d18c1a1
- commit date: 2025-10-21
- overall geometric mean: 1.075x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| html5lib       | 67.0 ms                                                      | 63.2 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.49x faster                                                    |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 470 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.38x faster                                                    |
| async_tree_none            | 354 ms                                                       | 260 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 472 ms: 1.35x faster                                                    |
| async_generators           | 377 ms                                                       | 339 ms: 1.11x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.7 ms: 1.04x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 62.7 ms: 1.23x faster                                                   |
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| nbody          | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                   |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                   |
| regex_compile  | 132 ms                                                       | 139 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 8.79 ms: 1.20x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 185 us: 1.13x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 52.7 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 76.6 ms: 1.12x faster                                                   |
| json_loads           | 27.0 us                                                      | 25.7 us: 1.05x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 304 us: 1.03x slower                                                    |
| xml_etree_parse      | 136 ms                                                       | 148 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                            |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                   |
| python_startup         | 11.0 ms                                                      | 12.8 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.7 ms: 1.09x faster                                                   |
| mako            | 11.3 ms                                                      | 11.0 ms: 1.03x faster                                                   |
| django_template | 34.1 ms                                                      | 33.4 ms: 1.02x faster                                                   |
| genshi_xml      | 48.8 ms                                                      | 50.1 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.0 ms: 2.06x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.18 sec: 2.00x faster                                                  |
| richards_super             | 51.6 ms                                                      | 26.8 ms: 1.93x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 22.0 us: 1.77x faster                                                   |
| deepcopy                   | 355 us                                                       | 229 us: 1.55x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.49x faster                                                    |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 470 ms: 1.42x faster                                                    |
| scimark_fft                | 349 ms                                                       | 247 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.38x faster                                                    |
| async_tree_none            | 354 ms                                                       | 260 ms: 1.36x faster                                                    |
| scimark_sor                | 134 ms                                                       | 99.3 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 472 ms: 1.35x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.33 us: 1.33x faster                                                   |
| spectral_norm              | 111 ms                                                       | 83.6 ms: 1.33x faster                                                   |
| logging_silent             | 103 ns                                                       | 78.9 ns: 1.30x faster                                                   |
| float                      | 77.5 ms                                                      | 62.7 ms: 1.23x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 8.79 ms: 1.20x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.01 ms: 1.17x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 96.6 ms: 1.17x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 56.0 ms: 1.17x faster                                                   |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                    |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 185 us: 1.13x faster                                                    |
| pyflate                    | 449 ms                                                       | 396 ms: 1.13x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 653 ms: 1.13x faster                                                    |
| comprehensions             | 16.5 us                                                      | 14.6 us: 1.13x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.94 sec: 1.13x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 52.7 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.78 ms: 1.12x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 76.6 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 339 ms: 1.11x faster                                                    |
| coverage                   | 83.0 ms                                                      | 75.2 ms: 1.10x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 19.7 ms: 1.09x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.37 sec: 1.09x faster                                                  |
| chaos                      | 57.3 ms                                                      | 52.9 ms: 1.08x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 63.2 ms: 1.06x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.7 ms: 1.06x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                   |
| json_loads                 | 27.0 us                                                      | 25.7 us: 1.05x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.87 us: 1.05x faster                                                   |
| fannkuch                   | 370 ms                                                       | 353 ms: 1.05x faster                                                    |
| generators                 | 28.8 ms                                                      | 27.6 ms: 1.04x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 148 us: 1.04x faster                                                    |
| logging_format             | 6.84 us                                                      | 6.58 us: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.7 ms: 1.04x faster                                                   |
| thrift                     | 778 us                                                       | 753 us: 1.03x faster                                                    |
| mako                       | 11.3 ms                                                      | 11.0 ms: 1.03x faster                                                   |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                   |
| django_template            | 34.1 ms                                                      | 33.4 ms: 1.02x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 66.6 ms: 1.02x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.88 ms: 1.02x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 73.5 ms: 1.02x faster                                                   |
| json                       | 4.93 ms                                                      | 4.84 ms: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                   |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.1 ms: 1.03x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 81.1 ms: 1.03x slower                                                   |
| sympy_expand               | 457 ms                                                       | 475 ms: 1.04x slower                                                    |
| meteor_contest             | 102 ms                                                       | 106 ms: 1.04x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| regex_compile              | 132 ms                                                       | 139 ms: 1.05x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 970 us: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.20 sec: 1.07x slower                                                  |
| raytrace                   | 253 ms                                                       | 273 ms: 1.08x slower                                                    |
| xml_etree_parse            | 136 ms                                                       | 148 ms: 1.08x slower                                                    |
| nbody                      | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.8 ms: 1.17x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.51 ms: 1.43x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 2.02 ms: 1.51x slower                                                   |
| telco                      | 7.82 ms                                                      | 157 ms: 20.03x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                            |

Benchmark hidden because not significant (3): tomli_loads, docutils, xml_etree_iterparse
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251021-3.15.0a1+-d18c1a1-CLANG,JIT/bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.21x