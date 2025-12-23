# Results vs. 3.13.0rc2

- fork: diegorusso
- ref: executor_register
- machine: linux-x86_64
- commit hash: 92c1f91
- commit date: 2025-12-22
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                  |
| html5lib       | 67.0 ms                                                      | 65.6 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 584 ms: 1.56x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                    |
| async_tree_none            | 354 ms                                                       | 241 ms: 1.47x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                    |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 59.6 ms: 1.30x faster                                                   |
| nbody          | 85.1 ms                                                      | 75.9 ms: 1.12x faster                                                   |
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                    |
| Geometric mean | (ref)                                                        | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                   |
| regex_compile  | 132 ms                                                       | 122 ms: 1.09x faster                                                    |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 174 us: 1.21x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.3 ms: 1.14x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 9.44 ms: 1.12x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 77.2 ms: 1.11x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 53.7 ms: 1.10x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 277 us: 1.06x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.94 sec: 1.03x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 53.6 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 17.8 ms: 2.54x faster                                                   |
| richards_super             | 51.6 ms                                                      | 21.6 ms: 2.40x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                                  |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 24.9 us: 1.57x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 584 ms: 1.56x faster                                                    |
| go                         | 141 ms                                                       | 91.7 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                    |
| deepcopy                   | 355 us                                                       | 240 us: 1.48x faster                                                    |
| async_tree_none            | 354 ms                                                       | 241 ms: 1.47x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                    |
| scimark_fft                | 349 ms                                                       | 261 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                    |
| scimark_sor                | 134 ms                                                       | 103 ms: 1.31x faster                                                    |
| float                      | 77.5 ms                                                      | 59.6 ms: 1.30x faster                                                   |
| spectral_norm              | 111 ms                                                       | 87.6 ms: 1.27x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.2 ms: 1.25x faster                                                   |
| logging_silent             | 103 ns                                                       | 82.1 ns: 1.25x faster                                                   |
| pyflate                    | 449 ms                                                       | 363 ms: 1.24x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 174 us: 1.21x faster                                                    |
| deltablue                  | 3.12 ms                                                      | 2.64 ms: 1.18x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 639 ms: 1.15x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.31 sec: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.3 ms: 1.14x faster                                                   |
| nbody                      | 85.1 ms                                                      | 75.9 ms: 1.12x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.44 ms: 1.12x faster                                                   |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.00 sec: 1.11x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 77.2 ms: 1.11x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 53.7 ms: 1.10x faster                                                   |
| chaos                      | 57.3 ms                                                      | 52.2 ms: 1.10x faster                                                   |
| regex_compile              | 132 ms                                                       | 122 ms: 1.09x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.09x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                   |
| thrift                     | 778 us                                                       | 731 us: 1.06x faster                                                    |
| scimark_lu                 | 113 ms                                                       | 106 ms: 1.06x faster                                                    |
| pickle_pure_python         | 294 us                                                       | 277 us: 1.06x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                    |
| fannkuch                   | 370 ms                                                       | 352 ms: 1.05x faster                                                    |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                    |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.50 ms: 1.05x faster                                                   |
| comprehensions             | 16.5 us                                                      | 15.8 us: 1.04x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 72.2 ms: 1.04x faster                                                   |
| meteor_contest             | 102 ms                                                       | 98.2 ms: 1.03x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.94 sec: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 65.8 ms: 1.03x faster                                                   |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                    |
| logging_simple             | 6.16 us                                                      | 6.02 us: 1.02x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 65.6 ms: 1.02x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.77 us: 1.01x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.97 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.01x slower                                                    |
| generators                 | 28.8 ms                                                      | 29.4 ms: 1.02x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.02x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                   |
| raytrace                   | 253 ms                                                       | 263 ms: 1.04x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 85.6 ms: 1.09x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 171 ms: 1.10x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 53.6 ms: 1.10x slower                                                   |
| sympy_expand               | 457 ms                                                       | 511 ms: 1.12x slower                                                    |
| sympy_str                  | 275 ms                                                       | 308 ms: 1.12x slower                                                    |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.24 ms: 1.35x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 214 ms: 19.45x slower                                                   |
| telco                      | 7.82 ms                                                      | 161 ms: 20.63x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                            |

Benchmark hidden because not significant (4): pylint, json, genshi_text, coverage
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251222-3.15.0a3+-92c1f91-JIT/bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x