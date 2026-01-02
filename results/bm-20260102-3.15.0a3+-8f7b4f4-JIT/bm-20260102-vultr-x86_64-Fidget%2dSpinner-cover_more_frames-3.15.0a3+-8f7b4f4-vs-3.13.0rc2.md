# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: linux-x86_64
- commit hash: 8f7b4f4
- commit date: 2026-01-02
- overall geometric mean: 1.084x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                          |
| docutils       | 2.62 sec                                                     | 2.68 sec: 1.02x slower                                                        |
| html5lib       | 67.0 ms                                                      | 64.0 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 545 ms: 1.61x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 578 ms: 1.58x faster                                                          |
| async_tree_memoization     | 461 ms                                                       | 296 ms: 1.56x faster                                                          |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                          |
| async_tree_none_tg         | 336 ms                                                       | 237 ms: 1.42x faster                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 481 ms: 1.38x faster                                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 300 ms: 1.38x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                          |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                          |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                         |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 57.4 ms: 1.35x faster                                                         |
| nbody          | 85.1 ms                                                      | 74.4 ms: 1.14x faster                                                         |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                          |
| Geometric mean | (ref)                                                        | 1.18x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                         |
| regex_compile  | 132 ms                                                       | 121 ms: 1.09x faster                                                          |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                          |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 175 us: 1.20x faster                                                          |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                         |
| xml_etree_generate   | 85.4 ms                                                      | 77.0 ms: 1.11x faster                                                         |
| json_dumps           | 10.5 ms                                                      | 9.51 ms: 1.11x faster                                                         |
| xml_etree_process    | 59.3 ms                                                      | 53.9 ms: 1.10x faster                                                         |
| pickle_pure_python   | 294 us                                                       | 277 us: 1.06x faster                                                          |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                          |
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                        |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.38 ms: 1.00x faster                                                         |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                         |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                         |
| genshi_text     | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                         |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                         |
| genshi_xml      | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                         |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 17.9 ms: 2.52x faster                                                         |
| richards_super             | 51.6 ms                                                      | 21.6 ms: 2.39x faster                                                         |
| mdp                        | 2.36 sec                                                     | 1.35 sec: 1.74x faster                                                        |
| async_tree_io              | 876 ms                                                       | 545 ms: 1.61x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 578 ms: 1.58x faster                                                          |
| deepcopy_memo              | 39.1 us                                                      | 24.9 us: 1.57x faster                                                         |
| async_tree_memoization     | 461 ms                                                       | 296 ms: 1.56x faster                                                          |
| go                         | 141 ms                                                       | 91.8 ms: 1.53x faster                                                         |
| deepcopy                   | 355 us                                                       | 240 us: 1.48x faster                                                          |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                          |
| async_tree_none_tg         | 336 ms                                                       | 237 ms: 1.42x faster                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 481 ms: 1.38x faster                                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 300 ms: 1.38x faster                                                          |
| scimark_fft                | 349 ms                                                       | 259 ms: 1.35x faster                                                          |
| float                      | 77.5 ms                                                      | 57.4 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                          |
| scimark_sor                | 134 ms                                                       | 103 ms: 1.31x faster                                                          |
| spectral_norm              | 111 ms                                                       | 86.9 ms: 1.28x faster                                                         |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.1 ms: 1.26x faster                                                         |
| logging_silent             | 103 ns                                                       | 83.3 ns: 1.23x faster                                                         |
| pyflate                    | 449 ms                                                       | 365 ms: 1.23x faster                                                          |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.23x faster                                                         |
| unpickle_pure_python       | 210 us                                                       | 175 us: 1.20x faster                                                          |
| deltablue                  | 3.12 ms                                                      | 2.65 ms: 1.18x faster                                                         |
| pprint_safe_repr           | 738 ms                                                       | 640 ms: 1.15x faster                                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.30 sec: 1.15x faster                                                        |
| nbody                      | 85.1 ms                                                      | 74.4 ms: 1.14x faster                                                         |
| scimark_lu                 | 113 ms                                                       | 98.8 ms: 1.14x faster                                                         |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                         |
| xml_etree_generate         | 85.4 ms                                                      | 77.0 ms: 1.11x faster                                                         |
| bpe_tokeniser              | 4.45 sec                                                     | 4.01 sec: 1.11x faster                                                        |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                         |
| json_dumps                 | 10.5 ms                                                      | 9.51 ms: 1.11x faster                                                         |
| chaos                      | 57.3 ms                                                      | 51.9 ms: 1.10x faster                                                         |
| xml_etree_process          | 59.3 ms                                                      | 53.9 ms: 1.10x faster                                                         |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.09x faster                                                         |
| regex_compile              | 132 ms                                                       | 121 ms: 1.09x faster                                                          |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                         |
| thrift                     | 778 us                                                       | 723 us: 1.08x faster                                                          |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                          |
| logging_simple             | 6.16 us                                                      | 5.77 us: 1.07x faster                                                         |
| pickle_pure_python         | 294 us                                                       | 277 us: 1.06x faster                                                          |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                                         |
| logging_format             | 6.84 us                                                      | 6.48 us: 1.06x faster                                                         |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                          |
| html5lib                   | 67.0 ms                                                      | 64.0 ms: 1.05x faster                                                         |
| fannkuch                   | 370 ms                                                       | 354 ms: 1.04x faster                                                          |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                         |
| dulwich_log                | 74.8 ms                                                      | 71.8 ms: 1.04x faster                                                         |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                          |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                        |
| meteor_contest             | 102 ms                                                       | 98.3 ms: 1.03x faster                                                         |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                        |
| crypto_pyaes               | 67.9 ms                                                      | 65.9 ms: 1.03x faster                                                         |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                         |
| coverage                   | 83.0 ms                                                      | 81.8 ms: 1.01x faster                                                         |
| python_startup_no_site     | 7.39 ms                                                      | 7.38 ms: 1.00x faster                                                         |
| hexiom                     | 5.99 ms                                                      | 6.03 ms: 1.01x slower                                                         |
| json                       | 4.93 ms                                                      | 5.01 ms: 1.02x slower                                                         |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                          |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                         |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.02x slower                                                         |
| docutils                   | 2.62 sec                                                     | 2.68 sec: 1.02x slower                                                        |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                          |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                         |
| genshi_xml                 | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                         |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                          |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                         |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                         |
| nqueens                    | 78.6 ms                                                      | 83.7 ms: 1.07x slower                                                         |
| sympy_sum                  | 156 ms                                                       | 170 ms: 1.09x slower                                                          |
| sympy_str                  | 275 ms                                                       | 306 ms: 1.12x slower                                                          |
| sympy_expand               | 457 ms                                                       | 519 ms: 1.14x slower                                                          |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                         |
| bench_thread_pool          | 919 us                                                       | 1.30 ms: 1.42x slower                                                         |
| gc_traversal               | 3.14 ms                                                      | 4.47 ms: 1.42x slower                                                         |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                         |
| bench_mp_pool              | 11.0 ms                                                      | 220 ms: 19.99x slower                                                         |
| telco                      | 7.82 ms                                                      | 160 ms: 20.51x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                                  |

Benchmark hidden because not significant (4): pylint, sqlite_synth, typing_runtime_protocols, generators
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260102-3.15.0a3+-8f7b4f4-JIT/bm-20260102-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x