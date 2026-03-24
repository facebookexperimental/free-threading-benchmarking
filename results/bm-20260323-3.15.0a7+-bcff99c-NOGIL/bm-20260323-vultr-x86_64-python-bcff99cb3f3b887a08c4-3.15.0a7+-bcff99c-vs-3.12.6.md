# Results vs. 3.12.6

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: linux-x86_64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.029x slower
- HPT reliability: 80.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                   |
| docutils       | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 602 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 547 ms: 1.31x faster                                                   |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.3 ms: 1.10x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.00 ms: 1.05x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                  |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.2 ms: 1.16x slower                                                  |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.77 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                  |
| django_template | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                  |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 602 ms: 1.84x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.58x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.02 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                   |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 547 ms: 1.31x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.3 us: 1.29x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.92 us: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.5 ms: 1.13x faster                                                  |
| float                      | 80.8 ms                                                | 73.3 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                 |
| comprehensions             | 19.8 us                                                | 18.4 us: 1.08x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                   |
| pylint                     | 319 ms                                                 | 300 ms: 1.06x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 3.00 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                   |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                 |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.51 ms: 1.02x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.84 us: 1.03x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                  |
| scimark_fft                | 342 ms                                                 | 354 ms: 1.04x slower                                                   |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.48 ms: 1.05x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                  |
| sympy_str                  | 292 ms                                                 | 310 ms: 1.06x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 801 ms: 1.08x slower                                                   |
| nqueens                    | 80.1 ms                                                | 86.4 ms: 1.08x slower                                                  |
| logging_format             | 7.35 us                                                | 7.94 us: 1.08x slower                                                  |
| json                       | 5.02 ms                                                | 5.44 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                                 |
| sympy_expand               | 468 ms                                                 | 516 ms: 1.10x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                  |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.7 ms: 1.14x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.5 ms: 1.15x slower                                                  |
| django_template            | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                  |
| thrift                     | 791 us                                                 | 911 us: 1.15x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 78.9 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.2 ms: 1.16x slower                                                  |
| richards                   | 45.9 ms                                                | 53.2 ms: 1.16x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                                   |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.21x slower                                                   |
| fannkuch                   | 372 ms                                                 | 460 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.69 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.77 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.37x slower                                                  |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                   |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.49 ms: 1.58x slower                                                  |
| coverage                   | 71.4 ms                                                | 113 ms: 1.58x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.61x slower                                                  |
| telco                      | 6.53 ms                                                | 172 ms: 26.41x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): coroutines, regex_compile
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 80.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x