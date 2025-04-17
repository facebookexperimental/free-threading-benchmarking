# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 956e5d1
- commit date: 2025-04-16
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                                     |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.77x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                     |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 507 ms: 1.41x faster                                                     |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                    |
| nbody          | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                    |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                    |
| regex_compile  | 142 ms                                                 | 123 ms: 1.15x faster                                                     |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                     |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.06x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 302 us: 1.02x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 84.6 ms: 1.01x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                    |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                    |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.52x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                    |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                    |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.14x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.77x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                     |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 507 ms: 1.41x faster                                                     |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 29.1 us: 1.38x faster                                                    |
| go                         | 139 ms                                                 | 106 ms: 1.31x faster                                                     |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.21x faster                                                    |
| raytrace                   | 299 ms                                                 | 247 ms: 1.21x faster                                                     |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                     |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                    |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 67.6 ms: 1.17x faster                                                    |
| chaos                      | 62.8 ms                                                | 54.0 ms: 1.16x faster                                                    |
| regex_compile              | 142 ms                                                 | 123 ms: 1.15x faster                                                     |
| spectral_norm              | 110 ms                                                 | 95.7 ms: 1.15x faster                                                    |
| float                      | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                    |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                     |
| richards                   | 45.9 ms                                                | 40.4 ms: 1.14x faster                                                    |
| pyflate                    | 448 ms                                                 | 397 ms: 1.13x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                    |
| logging_silent             | 109 ns                                                 | 96.9 ns: 1.12x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.12x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                   |
| richards_super             | 51.9 ms                                                | 46.4 ms: 1.12x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 61.5 ms: 1.11x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.7 ms: 1.11x faster                                                    |
| logging_simple             | 6.63 us                                                | 5.98 us: 1.11x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.09x faster                                                     |
| logging_format             | 7.35 us                                                | 6.73 us: 1.09x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                    |
| sympy_str                  | 292 ms                                                 | 268 ms: 1.09x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.73 ms: 1.08x faster                                                    |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 701 ms: 1.06x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.06x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| scimark_fft                | 342 ms                                                 | 325 ms: 1.05x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                    |
| nqueens                    | 80.1 ms                                                | 76.7 ms: 1.04x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                     |
| genshi_xml                 | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                    |
| sympy_expand               | 468 ms                                                 | 454 ms: 1.03x faster                                                     |
| pickle_pure_python         | 308 us                                                 | 302 us: 1.02x faster                                                     |
| nbody                      | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 84.6 ms: 1.01x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 115 ms: 1.01x slower                                                     |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                    |
| fannkuch                   | 372 ms                                                 | 377 ms: 1.01x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                    |
| django_template            | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.49 ms: 1.02x slower                                                    |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                    |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                    |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| telco                      | 6.53 ms                                                | 7.24 ms: 1.11x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                    |
| coverage                   | 71.4 ms                                                | 80.5 ms: 1.13x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.29 ms: 1.24x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.52x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 87.7 ms: 8.12x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250416-3.14.0a7+-956e5d1/bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x