# Results vs. 3.12.6

- fork: python
- ref: 0eeaa0ef8bf60fd3b144
- machine: linux-x86_64
- commit hash: 0eeaa0e
- commit date: 2025-05-05
- overall geometric mean: 1.141x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 243 ms: 1.08x faster                                                   |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                   |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.1 ms: 1.14x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.1 ms: 1.20x faster                                                  |
| nbody          | 89.3 ms                                                | 82.3 ms: 1.09x faster                                                  |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 201 us: 1.10x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 81.1 ms: 1.05x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 293 us: 1.05x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 56.3 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 95.1 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 27.3 us: 1.03x slower                                                  |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 45.4 ms: 1.10x faster                                                  |
| django_template | 34.7 ms                                                | 32.7 ms: 1.06x faster                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.11 sec: 2.18x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                   |
| deepcopy                   | 352 us                                                 | 231 us: 1.52x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 27.5 us: 1.46x faster                                                  |
| go                         | 139 ms                                                 | 102 ms: 1.37x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.0 us: 1.32x faster                                                  |
| logging_silent             | 109 ns                                                 | 84.1 ns: 1.30x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.39 us: 1.29x faster                                                  |
| raytrace                   | 299 ms                                                 | 236 ms: 1.27x faster                                                   |
| chaos                      | 62.8 ms                                                | 50.5 ms: 1.24x faster                                                  |
| spectral_norm              | 110 ms                                                 | 89.1 ms: 1.24x faster                                                  |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.22x faster                                                   |
| richards                   | 45.9 ms                                                | 38.1 ms: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 67.1 ms: 1.20x faster                                                  |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                                   |
| generators                 | 32.2 ms                                                | 27.0 ms: 1.20x faster                                                  |
| richards_super             | 51.9 ms                                                | 43.6 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                  |
| genshi_text                | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.18x faster                                                 |
| regex_compile              | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| pylint                     | 319 ms                                                 | 274 ms: 1.16x faster                                                   |
| logging_format             | 7.35 us                                                | 6.35 us: 1.16x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.77 us: 1.15x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.15x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.0 ms: 1.14x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.43 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.1 ms: 1.14x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.07 ms: 1.12x faster                                                  |
| sympy_str                  | 292 ms                                                 | 259 ms: 1.12x faster                                                   |
| pyflate                    | 448 ms                                                 | 399 ms: 1.12x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 148 ms: 1.12x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                   |
| nqueens                    | 80.1 ms                                                | 72.0 ms: 1.11x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 45.4 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.0 ms: 1.10x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 201 us: 1.10x faster                                                   |
| nbody                      | 89.3 ms                                                | 82.3 ms: 1.09x faster                                                  |
| 2to3                       | 264 ms                                                 | 243 ms: 1.08x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| sympy_expand               | 468 ms                                                 | 437 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                  |
| django_template            | 34.7 ms                                                | 32.7 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 707 ms: 1.05x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 81.1 ms: 1.05x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 293 us: 1.05x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 56.3 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                   |
| scimark_fft                | 342 ms                                                 | 336 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 95.1 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                  |
| meteor_contest             | 104 ms                                                 | 105 ms: 1.01x slower                                                   |
| fannkuch                   | 372 ms                                                 | 379 ms: 1.02x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.3 us: 1.03x slower                                                  |
| telco                      | 6.53 ms                                                | 6.74 ms: 1.03x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                   |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.11 ms: 1.16x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.21 ms: 1.22x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.78x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 87.2 ms: 8.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (2): json, asyncio_websockets
Ignored benchmarks (24) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250505-3.14.0a7+-0eeaa0e-CLANG/bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.141x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.17x