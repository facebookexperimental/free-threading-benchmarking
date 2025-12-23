# Results vs. 3.13.0rc2

- fork: python
- ref: ff7f62eb2333ac2a2ce2
- machine: linux-x86_64
- commit hash: ff7f62e
- commit date: 2025-12-22
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.68 sec: 1.02x slower                                                 |
| html5lib       | 67.0 ms                                                      | 64.2 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 558 ms: 1.57x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 592 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 488 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                   |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                  |
| nbody          | 85.1 ms                                                      | 73.3 ms: 1.16x faster                                                  |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                        | 1.17x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.63 ms: 1.17x faster                                                  |
| regex_compile  | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                        | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 176 us: 1.19x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.7 ms: 1.13x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.47 ms: 1.11x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 54.1 ms: 1.10x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 78.0 ms: 1.09x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 278 us: 1.06x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.37 ms: 1.00x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                  |
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                  |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 53.4 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.4 ms: 2.46x faster                                                  |
| richards_super             | 51.6 ms                                                      | 22.0 ms: 2.35x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                                 |
| async_tree_io              | 876 ms                                                       | 558 ms: 1.57x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 592 ms: 1.54x faster                                                   |
| go                         | 141 ms                                                       | 91.8 ms: 1.53x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 25.6 us: 1.53x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                   |
| deepcopy                   | 355 us                                                       | 244 us: 1.46x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 488 ms: 1.36x faster                                                   |
| scimark_fft                | 349 ms                                                       | 258 ms: 1.36x faster                                                   |
| scimark_sor                | 134 ms                                                       | 99.6 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                   |
| spectral_norm              | 111 ms                                                       | 85.6 ms: 1.30x faster                                                  |
| float                      | 77.5 ms                                                      | 60.5 ms: 1.28x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.8 ms: 1.26x faster                                                  |
| logging_silent             | 103 ns                                                       | 82.4 ns: 1.25x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.50 us: 1.25x faster                                                  |
| pyflate                    | 449 ms                                                       | 365 ms: 1.23x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 176 us: 1.19x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 2.63 ms: 1.19x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.63 ms: 1.17x faster                                                  |
| nbody                      | 85.1 ms                                                      | 73.3 ms: 1.16x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 639 ms: 1.15x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.30 sec: 1.15x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.7 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 3.99 sec: 1.11x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.47 ms: 1.11x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 54.1 ms: 1.10x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 78.0 ms: 1.09x faster                                                  |
| regex_compile              | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                  |
| chaos                      | 57.3 ms                                                      | 53.2 ms: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.38 ms: 1.08x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 105 ms: 1.07x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                  |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                  |
| thrift                     | 778 us                                                       | 732 us: 1.06x faster                                                   |
| pickle_pure_python         | 294 us                                                       | 278 us: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 71.5 ms: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| fannkuch                   | 370 ms                                                       | 354 ms: 1.05x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 64.2 ms: 1.04x faster                                                  |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.93 us: 1.04x faster                                                  |
| meteor_contest             | 102 ms                                                       | 98.1 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.63 us: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.0 ms: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.2 ms: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.2 us: 1.01x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.37 ms: 1.00x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.06 ms: 1.01x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.68 sec: 1.02x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.5 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 20.4 ms: 1.03x slower                                                  |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 84.4 ms: 1.07x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 170 ms: 1.09x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 53.4 ms: 1.09x slower                                                  |
| sympy_expand               | 457 ms                                                       | 507 ms: 1.11x slower                                                   |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.43x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.66 ms: 1.48x slower                                                  |
| telco                      | 7.82 ms                                                      | 164 ms: 20.93x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 244 ms: 22.16x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (3): pylint, sqlite_synth, json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251222-3.15.0a3+-ff7f62e-JIT/bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x