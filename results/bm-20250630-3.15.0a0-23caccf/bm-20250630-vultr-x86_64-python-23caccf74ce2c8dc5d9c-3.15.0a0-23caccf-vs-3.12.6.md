# Results vs. 3.12.6

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: linux-x86_64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.109x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| html5lib       | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.7 ms: 1.11x faster                                                 |
| nbody          | 89.3 ms                                                | 88.3 ms: 1.01x faster                                                 |
| pidigits       | 184 ms                                                 | 203 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.03x slower                                                 |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 93.3 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.00x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.5 ms: 1.00x faster                                                 |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.1 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.0 ms: 1.18x faster                                                 |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 27.8 ms: 1.16x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.8 ms: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 97.1 ms: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                |
| pyflate                    | 448 ms                                                 | 399 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.0 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.2 ms: 1.11x faster                                                 |
| logging_silent             | 109 ns                                                 | 97.7 ns: 1.11x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.97 us: 1.11x faster                                                 |
| float                      | 80.8 ms                                                | 72.7 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.7 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.6 ms: 1.11x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| logging_format             | 7.35 us                                                | 6.69 us: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.64 ms: 1.09x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 691 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 740 us: 1.07x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.26 ms: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.5 ms: 1.04x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.3 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.6 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| scimark_fft                | 342 ms                                                 | 337 ms: 1.01x faster                                                  |
| nbody                      | 89.3 ms                                                | 88.3 ms: 1.01x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                 |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.00x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.00x faster                                                  |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| fannkuch                   | 372 ms                                                 | 389 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| pidigits                   | 184 ms                                                 | 203 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.89 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.39 ms: 1.13x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.33 ms: 1.25x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.74x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 99.0 ms: 9.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.109x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x