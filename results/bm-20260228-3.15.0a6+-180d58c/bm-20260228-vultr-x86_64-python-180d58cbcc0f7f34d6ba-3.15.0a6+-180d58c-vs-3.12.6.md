# Results vs. 3.12.6

- fork: python
- ref: 180d58cbcc0f7f34d6ba
- machine: linux-x86_64
- commit hash: 180d58c
- commit date: 2026-02-28
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 61.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 569 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 591 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.47x faster                                                   |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                  |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.02 ms: 1.05x faster                                                  |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.5 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 84.9 ms: 1.14x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.41 ms: 1.03x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.2 ms: 1.07x faster                                                  |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.8 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 569 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 591 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.4 us: 1.53x faster                                                  |
| deepcopy                   | 352 us                                                 | 233 us: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.47x faster                                                   |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.53 us: 1.22x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.22x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.4 us: 1.21x faster                                                  |
| spectral_norm              | 110 ms                                                 | 91.8 ms: 1.20x faster                                                  |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                   |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.5 ms: 1.17x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.1 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 84.9 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                  |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                   |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                   |
| scimark_fft                | 342 ms                                                 | 307 ms: 1.11x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.99 us: 1.11x faster                                                  |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.75 us: 1.09x faster                                                  |
| richards                   | 45.9 ms                                                | 42.3 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 416 ms: 1.08x faster                                                   |
| richards_super             | 51.9 ms                                                | 48.2 ms: 1.08x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 64.1 ms: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 3.02 ms: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 709 ms: 1.05x faster                                                   |
| sympy_str                  | 292 ms                                                 | 279 ms: 1.05x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 159 ms: 1.05x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.32 ms: 1.04x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.9 ms: 1.03x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.1 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                   |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                  |
| thrift                     | 791 us                                                 | 780 us: 1.02x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.38 ms: 1.00x faster                                                  |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 475 ms: 1.02x slower                                                   |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.41 ms: 1.03x slower                                                  |
| fannkuch                   | 372 ms                                                 | 387 ms: 1.04x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.08x slower                                                  |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.5 ms: 1.09x slower                                                  |
| coverage                   | 71.4 ms                                                | 82.9 ms: 1.16x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.46 ms: 1.29x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 246 ms: 22.82x slower                                                  |
| telco                      | 6.53 ms                                                | 156 ms: 23.94x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): coroutines, nbody, pickle_pure_python, genshi_xml
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260228-3.15.0a6+-180d58c/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x