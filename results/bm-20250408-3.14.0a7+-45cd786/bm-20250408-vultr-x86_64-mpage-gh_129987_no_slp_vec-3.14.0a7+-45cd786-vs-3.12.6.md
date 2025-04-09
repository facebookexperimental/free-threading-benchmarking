# Results vs. 3.12.6

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 45cd786
- commit date: 2025-04-08
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 245 ms: 1.07x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 617 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 504 ms: 1.42x faster                                                  |
| async_generators           | 384 ms                                                 | 324 ms: 1.18x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.5 ms: 1.18x faster                                                 |
| nbody          | 89.3 ms                                                | 83.2 ms: 1.07x faster                                                 |
| pidigits       | 184 ms                                                 | 202 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.17x faster                                                 |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.81 sec: 1.17x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.61 ms: 1.20x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                 |
| mako           | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.15x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 617 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 504 ms: 1.42x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.8 us: 1.40x faster                                                 |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| go                         | 139 ms                                                 | 106 ms: 1.31x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.22x faster                                                 |
| raytrace                   | 299 ms                                                 | 246 ms: 1.22x faster                                                  |
| spectral_norm              | 110 ms                                                 | 92.1 ms: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| chaos                      | 62.8 ms                                                | 52.9 ms: 1.19x faster                                                 |
| async_generators           | 384 ms                                                 | 324 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.2 ms: 1.18x faster                                                 |
| float                      | 80.8 ms                                                | 68.5 ms: 1.18x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 67.0 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.81 sec: 1.17x faster                                                |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.17x faster                                                 |
| pylint                     | 319 ms                                                 | 276 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 66.5 ms: 1.15x faster                                                 |
| richards                   | 45.9 ms                                                | 40.1 ms: 1.15x faster                                                 |
| logging_silent             | 109 ns                                                 | 95.4 ns: 1.14x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 60.1 ms: 1.14x faster                                                 |
| pyflate                    | 448 ms                                                 | 395 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                |
| logging_simple             | 6.63 us                                                | 5.86 us: 1.13x faster                                                 |
| richards_super             | 51.9 ms                                                | 45.9 ms: 1.13x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                 |
| logging_format             | 7.35 us                                                | 6.54 us: 1.12x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                                 |
| scimark_fft                | 342 ms                                                 | 310 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.61 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                  |
| 2to3                       | 264 ms                                                 | 245 ms: 1.07x faster                                                  |
| nbody                      | 89.3 ms                                                | 83.2 ms: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 695 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.06x faster                                                  |
| meteor_contest             | 104 ms                                                 | 97.3 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| nqueens                    | 80.1 ms                                                | 75.6 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| sympy_expand               | 468 ms                                                 | 457 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 371 ms: 1.00x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                 |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                 |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| telco                      | 6.53 ms                                                | 7.14 ms: 1.09x slower                                                 |
| pidigits                   | 184 ms                                                 | 202 ms: 1.09x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.7 ms: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 8.61 ms: 1.20x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.31 ms: 1.25x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (4): asyncio_websockets, scimark_lu, django_template, json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250408-3.14.0a7+-45cd786/bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.13x