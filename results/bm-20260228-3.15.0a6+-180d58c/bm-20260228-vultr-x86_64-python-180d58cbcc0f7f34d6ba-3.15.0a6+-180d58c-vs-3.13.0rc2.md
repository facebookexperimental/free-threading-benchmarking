# Results vs. 3.13.0rc2

- fork: python
- ref: 180d58cbcc0f7f34d6ba
- machine: linux-x86_64
- commit hash: 180d58c
- commit date: 2026-02-28
- overall geometric mean: 1.034x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 61.9 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 569 ms: 1.61x faster                                                   |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.6 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 200 ms: 1.08x faster                                                   |
| nbody          | 85.1 ms                                                      | 89.4 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.02 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.5 ms: 1.01x faster                                                  |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.9 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.85 sec: 1.08x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.5 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 569 ms: 1.61x faster                                                   |
| deepcopy                   | 355 us                                                       | 233 us: 1.53x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.4 us: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 106 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.53 us: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 91.8 ms: 1.21x faster                                                  |
| scimark_fft                | 349 ms                                                       | 307 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.9 ms: 1.12x faster                                                  |
| float                      | 77.5 ms                                                      | 69.6 ms: 1.11x faster                                                  |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 67.5 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.85 sec: 1.08x faster                                                 |
| pidigits                   | 217 ms                                                       | 200 ms: 1.08x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 61.9 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                       | 416 ms: 1.08x faster                                                   |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.38 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.3 ms: 1.07x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.1 ms: 1.06x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.5 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 709 ms: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 251 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.99 us: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 100 ns: 1.03x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 3.02 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.1 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.5 ms: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.01x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.75 us: 1.01x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.5 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.4 us: 1.00x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.01x slower                                                   |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.03x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                  |
| sympy_expand               | 457 ms                                                       | 475 ms: 1.04x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.05x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| fannkuch                   | 370 ms                                                       | 387 ms: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 89.4 ms: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.32 ms: 1.06x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.46 ms: 1.42x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 156 ms: 19.97x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 246 ms: 22.42x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (4): coverage, meteor_contest, raytrace, thrift
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260228-3.15.0a6+-180d58c/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x