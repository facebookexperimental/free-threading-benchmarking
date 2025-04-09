# Results vs. 3.12.6

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 93646c2
- commit date: 2025-04-08
- overall geometric mean: 1.118x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 245 ms: 1.08x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                  |
| async_generators           | 384 ms                                                 | 323 ms: 1.19x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.3 ms: 1.18x faster                                                 |
| nbody          | 89.3 ms                                                | 82.0 ms: 1.09x faster                                                 |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                 |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 301 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.7 ms: 1.00x faster                                                 |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 35.9 ms: 1.03x slower                                                 |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.14x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                  |
| deepcopy                   | 352 us                                                 | 248 us: 1.42x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.0 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                  |
| raytrace                   | 299 ms                                                 | 243 ms: 1.23x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.21x faster                                                 |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.21x faster                                                  |
| spectral_norm              | 110 ms                                                 | 91.9 ms: 1.20x faster                                                 |
| chaos                      | 62.8 ms                                                | 52.5 ms: 1.20x faster                                                 |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                                 |
| async_generators           | 384 ms                                                 | 323 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.19x faster                                                 |
| float                      | 80.8 ms                                                | 68.3 ms: 1.18x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 66.8 ms: 1.18x faster                                                 |
| logging_silent             | 109 ns                                                 | 92.8 ns: 1.17x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 66.7 ms: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 59.9 ms: 1.14x faster                                                 |
| richards                   | 45.9 ms                                                | 40.3 ms: 1.14x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.14x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.12x faster                                                |
| richards_super             | 51.9 ms                                                | 46.2 ms: 1.12x faster                                                 |
| logging_format             | 7.35 us                                                | 6.54 us: 1.12x faster                                                 |
| pyflate                    | 448 ms                                                 | 400 ms: 1.12x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.60 ms: 1.10x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.8 ms: 1.10x faster                                                 |
| nbody                      | 89.3 ms                                                | 82.0 ms: 1.09x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.16 ms: 1.09x faster                                                 |
| scimark_fft                | 342 ms                                                 | 314 ms: 1.09x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| 2to3                       | 264 ms                                                 | 245 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.08x faster                                                |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                |
| nqueens                    | 80.1 ms                                                | 75.5 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 705 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.3 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 301 us: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.7 ms: 1.00x faster                                                 |
| json                       | 5.02 ms                                                | 5.10 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.53 ms: 1.03x slower                                                 |
| django_template            | 34.7 ms                                                | 35.9 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                 |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                                  |
| telco                      | 6.53 ms                                                | 7.13 ms: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 80.6 ms: 1.13x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.4 ms: 8.18x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, fannkuch
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250408-3.14.0a7+-93646c2/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.12x