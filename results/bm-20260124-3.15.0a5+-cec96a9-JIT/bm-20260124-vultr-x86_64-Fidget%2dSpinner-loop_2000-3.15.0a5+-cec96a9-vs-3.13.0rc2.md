# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: loop_2000
- machine: linux-x86_64
- commit hash: cec96a9
- commit date: 2026-01-24
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                |
| html5lib       | 67.0 ms                                                      | 62.9 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 555 ms: 1.65x faster                                                  |
| async_tree_io              | 876 ms                                                       | 541 ms: 1.62x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 292 ms: 1.58x faster                                                  |
| async_tree_none            | 354 ms                                                       | 236 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 479 ms: 1.39x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                  |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 57.9 ms: 1.34x faster                                                 |
| nbody          | 85.1 ms                                                      | 72.8 ms: 1.17x faster                                                 |
| pidigits       | 217 ms                                                       | 197 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.20x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.65 ms: 1.16x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                                 |
| regex_compile  | 132 ms                                                       | 122 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.67 sec: 1.20x faster                                                |
| unpickle_pure_python | 210 us                                                       | 178 us: 1.18x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.01 ms: 1.17x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 77.2 ms: 1.11x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 278 us: 1.06x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.11x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.37 ms: 1.00x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.3 ms: 1.11x faster                                                 |
| genshi_text     | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                 |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 51.3 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 17.4 ms: 2.59x faster                                                 |
| richards_super             | 51.6 ms                                                      | 21.0 ms: 2.46x faster                                                 |
| mdp                        | 2.36 sec                                                     | 1.36 sec: 1.74x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 22.6 us: 1.73x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 555 ms: 1.65x faster                                                  |
| async_tree_io              | 876 ms                                                       | 541 ms: 1.62x faster                                                  |
| deepcopy                   | 355 us                                                       | 222 us: 1.60x faster                                                  |
| scimark_sor                | 134 ms                                                       | 84.8 ms: 1.59x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 292 ms: 1.58x faster                                                  |
| async_tree_none            | 354 ms                                                       | 236 ms: 1.50x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 77.5 ms: 1.45x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 479 ms: 1.39x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                  |
| spectral_norm              | 111 ms                                                       | 80.9 ms: 1.37x faster                                                 |
| scimark_fft                | 349 ms                                                       | 255 ms: 1.37x faster                                                  |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                  |
| float                      | 77.5 ms                                                      | 57.9 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.38 us: 1.31x faster                                                 |
| logging_silent             | 103 ns                                                       | 81.2 ns: 1.26x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.1 ms: 1.25x faster                                                 |
| pyflate                    | 449 ms                                                       | 372 ms: 1.21x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.67 sec: 1.20x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.25 sec: 1.19x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 621 ms: 1.19x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 178 us: 1.18x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.01 ms: 1.17x faster                                                 |
| nbody                      | 85.1 ms                                                      | 72.8 ms: 1.17x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.65 ms: 1.16x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.09 ms: 1.15x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 2.74 ms: 1.14x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 3.94 sec: 1.13x faster                                                |
| xml_etree_process          | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 77.2 ms: 1.11x faster                                                 |
| mako                       | 11.3 ms                                                      | 10.3 ms: 1.11x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                 |
| pidigits                   | 217 ms                                                       | 197 ms: 1.10x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                                 |
| regex_compile              | 132 ms                                                       | 122 ms: 1.08x faster                                                  |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| fannkuch                   | 370 ms                                                       | 347 ms: 1.07x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 62.9 ms: 1.07x faster                                                 |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| pickle_pure_python         | 294 us                                                       | 278 us: 1.06x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.2 ms: 1.06x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 65.1 ms: 1.04x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 72.3 ms: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 756 us: 1.03x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| json                       | 4.93 ms                                                      | 4.86 ms: 1.01x faster                                                 |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.9 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.37 ms: 1.00x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                |
| logging_format             | 6.84 us                                                      | 7.00 us: 1.02x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.20 ms: 1.03x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                  |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 51.3 ms: 1.05x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 20.9 ms: 1.05x slower                                                 |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                  |
| sympy_expand               | 457 ms                                                       | 517 ms: 1.13x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 176 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.35 ms: 1.38x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 183 ms: 16.68x slower                                                 |
| telco                      | 7.82 ms                                                      | 166 ms: 21.22x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                          |

Benchmark hidden because not significant (5): sqlite_synth, logging_simple, nqueens, pylint, typing_runtime_protocols
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260124-3.15.0a5+-cec96a9-JIT/bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x