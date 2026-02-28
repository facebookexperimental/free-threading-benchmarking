# Results vs. 3.12.6

- fork: python
- ref: 180d58cbcc0f7f34d6ba
- machine: linux-x86_64
- commit hash: 180d58c
- commit date: 2026-02-28
- overall geometric mean: 1.031x slower
- HPT reliability: 83.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 287 ms: 1.09x slower                                                   |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 604 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 545 ms: 1.31x faster                                                   |
| async_generators           | 384 ms                                                 | 381 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.3 ms: 1.12x faster                                                  |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                  |
| regex_compile  | 142 ms                                                 | 140 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                  |
| regex_dna      | 168 ms                                                 | 168 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.4 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.8 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.7 ms: 1.18x slower                                                  |
| json_loads           | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.8 ms: 1.13x slower                                                  |
| django_template | 34.7 ms                                                | 40.9 ms: 1.18x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 604 ms: 1.84x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.08 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.39x faster                                                   |
| deepcopy                   | 352 us                                                 | 267 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 545 ms: 1.31x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.5 us: 1.28x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.21x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.93 us: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 72.3 ms: 1.12x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 294 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 89.4 ms: 1.08x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.6 us: 1.07x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.47 sec: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.05x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                 |
| regex_compile              | 142 ms                                                 | 140 ms: 1.01x faster                                                   |
| async_generators           | 384 ms                                                 | 381 ms: 1.01x faster                                                   |
| regex_v8                   | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                   |
| chaos                      | 62.8 ms                                                | 62.4 ms: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 168 ms: 1.00x slower                                                   |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                                   |
| generators                 | 32.2 ms                                                | 32.7 ms: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                   |
| scimark_fft                | 342 ms                                                 | 349 ms: 1.02x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.90 us: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| html5lib                   | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                  |
| pyflate                    | 448 ms                                                 | 468 ms: 1.05x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.50 ms: 1.05x slower                                                  |
| logging_format             | 7.35 us                                                | 7.83 us: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 800 ms: 1.08x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.73 ms: 1.08x slower                                                  |
| 2to3                       | 264 ms                                                 | 287 ms: 1.09x slower                                                   |
| json                       | 5.02 ms                                                | 5.48 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.11x slower                                                   |
| sympy_expand               | 468 ms                                                 | 525 ms: 1.12x slower                                                   |
| nqueens                    | 80.1 ms                                                | 90.1 ms: 1.12x slower                                                  |
| genshi_text                | 22.8 ms                                                | 25.8 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.8 ms: 1.14x slower                                                  |
| thrift                     | 791 us                                                 | 901 us: 1.14x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.8 ms: 1.15x slower                                                  |
| richards                   | 45.9 ms                                                | 53.0 ms: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.6 ms: 1.17x slower                                                  |
| django_template            | 34.7 ms                                                | 40.9 ms: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.7 ms: 1.18x slower                                                  |
| meteor_contest             | 104 ms                                                 | 123 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.31 ms: 1.21x slower                                                  |
| json_loads                 | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                   |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.47 ms: 1.34x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                   |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.64 ms: 1.74x slower                                                  |
| telco                      | 6.53 ms                                                | 174 ms: 26.71x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260228-3.15.0a6+-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6+-180d58c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 83.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x