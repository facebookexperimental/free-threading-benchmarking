# Results vs. 3.13.0rc2

- fork: python
- ref: fb8d8d9c9f9cbc94fa58
- machine: linux-x86_64
- commit hash: fb8d8d9
- commit date: 2026-03-22
- overall geometric mean: 1.032x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.52 sec: 1.04x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 566 ms: 1.61x faster                                                   |
| async_tree_io              | 876 ms                                                       | 585 ms: 1.50x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 528 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                   |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.1 ms: 1.10x faster                                                  |
| pidigits       | 217 ms                                                       | 206 ms: 1.05x faster                                                   |
| nbody          | 85.1 ms                                                      | 93.2 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.96 ms: 1.04x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                  |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 85.0 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.2 ms: 1.03x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 84.6 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.43 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 566 ms: 1.61x faster                                                   |
| deepcopy                   | 355 us                                                       | 235 us: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 585 ms: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 528 ms: 1.26x faster                                                   |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                   |
| spectral_norm              | 111 ms                                                       | 90.3 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.60 us: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                   |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.13x faster                                                   |
| pylint                     | 317 ms                                                       | 282 ms: 1.13x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.0 ms: 1.12x faster                                                  |
| pyflate                    | 449 ms                                                       | 402 ms: 1.11x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.1 ms: 1.10x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 69.2 ms: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.39 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.2 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.1 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.16 sec: 1.07x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.80 us: 1.06x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.0 ms: 1.06x faster                                                  |
| pidigits                   | 217 ms                                                       | 206 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.4 ms: 1.05x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.74 ms: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.96 ms: 1.04x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.52 sec: 1.04x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.04x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.8 ms: 1.04x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.2 ms: 1.03x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.62 us: 1.03x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                   |
| logging_silent             | 103 ns                                                       | 99.9 ns: 1.03x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 722 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.0 ms: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 84.6 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.6 ms: 1.00x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.5 us: 1.00x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.43 ms: 1.01x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 69.5 ms: 1.02x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                  |
| fannkuch                   | 370 ms                                                       | 383 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.04x slower                                                   |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.26 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                   |
| sympy_expand               | 457 ms                                                       | 482 ms: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                  |
| nbody                      | 85.1 ms                                                      | 93.2 ms: 1.09x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.33x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 262 ms: 23.80x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): thrift, meteor_contest, xml_etree_process
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260322-3.15.0a7+-fb8d8d9/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x