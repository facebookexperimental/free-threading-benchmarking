# Results vs. 3.12.6

- fork: nascheme
- ref: gc_check_rss
- machine: linux-x86_64
- commit hash: aabe31d
- commit date: 2025-05-04
- overall geometric mean: 1.007x faster
- HPT reliability: 90.90%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.06x slower                                             |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                           |
| html5lib       | 63.6 ms                                                | 65.8 ms: 1.03x slower                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                             |
| async_tree_io              | 1.08 sec                                               | 556 ms: 1.95x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 288 ms: 1.95x faster                                             |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                             |
| async_tree_memoization     | 555 ms                                                 | 318 ms: 1.74x faster                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 513 ms: 1.39x faster                                             |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                            |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                             |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                     |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.5 ms: 1.13x faster                                            |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                             |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                             |
| Geometric mean | (ref)                                                  | 1.07x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                            |
| regex_compile  | 142 ms                                                 | 146 ms: 1.02x slower                                             |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                            |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.5 ms: 1.11x faster                                            |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                             |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.02x slower                                           |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                             |
| pickle_pure_python   | 308 us                                                 | 331 us: 1.08x slower                                             |
| xml_etree_generate   | 85.2 ms                                                | 95.3 ms: 1.12x slower                                            |
| xml_etree_process    | 59.0 ms                                                | 68.2 ms: 1.16x slower                                            |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                            |
| json_dumps           | 10.4 ms                                                | 13.3 ms: 1.28x slower                                            |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.48 ms: 1.32x slower                                            |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                            |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.5 ms: 1.11x slower                                            |
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                            |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                            |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                            |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                             |
| async_tree_io              | 1.08 sec                                               | 556 ms: 1.95x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 288 ms: 1.95x faster                                             |
| gc_traversal               | 3.46 ms                                                | 1.86 ms: 1.86x faster                                            |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.81x faster                                           |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                             |
| async_tree_memoization     | 555 ms                                                 | 318 ms: 1.74x faster                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 513 ms: 1.39x faster                                             |
| deepcopy                   | 352 us                                                 | 297 us: 1.19x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 35.5 us: 1.13x faster                                            |
| float                      | 80.8 ms                                                | 71.5 ms: 1.13x faster                                            |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 87.5 ms: 1.11x faster                                            |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                            |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                            |
| generators                 | 32.2 ms                                                | 29.6 ms: 1.09x faster                                            |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                            |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                            |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.46 sec: 1.06x faster                                           |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                            |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.05x faster                                             |
| logging_silent             | 109 ns                                                 | 104 ns: 1.04x faster                                             |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                             |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                             |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                           |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                            |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                             |
| chaos                      | 62.8 ms                                                | 62.5 ms: 1.00x faster                                            |
| raytrace                   | 299 ms                                                 | 298 ms: 1.00x faster                                             |
| deepcopy_reduce            | 3.08 us                                                | 3.09 us: 1.01x slower                                            |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.02x slower                                           |
| regex_compile              | 142 ms                                                 | 146 ms: 1.02x slower                                             |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                           |
| json                       | 5.02 ms                                                | 5.19 ms: 1.03x slower                                            |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                             |
| html5lib                   | 63.6 ms                                                | 65.8 ms: 1.03x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                             |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                            |
| 2to3                       | 264 ms                                                 | 278 ms: 1.06x slower                                             |
| logging_simple             | 6.63 us                                                | 7.00 us: 1.06x slower                                            |
| pprint_safe_repr           | 743 ms                                                 | 795 ms: 1.07x slower                                             |
| pyflate                    | 448 ms                                                 | 480 ms: 1.07x slower                                             |
| pickle_pure_python         | 308 us                                                 | 331 us: 1.08x slower                                             |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.64 sec: 1.08x slower                                           |
| sqlalchemy_declarative     | 143 ms                                                 | 154 ms: 1.08x slower                                             |
| scimark_fft                | 342 ms                                                 | 370 ms: 1.08x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                            |
| logging_format             | 7.35 us                                                | 7.97 us: 1.08x slower                                            |
| sympy_integrate            | 20.5 ms                                                | 22.3 ms: 1.09x slower                                            |
| hexiom                     | 6.17 ms                                                | 6.71 ms: 1.09x slower                                            |
| sympy_str                  | 292 ms                                                 | 318 ms: 1.09x slower                                             |
| nqueens                    | 80.1 ms                                                | 87.9 ms: 1.10x slower                                            |
| genshi_xml                 | 50.2 ms                                                | 55.5 ms: 1.11x slower                                            |
| crypto_pyaes               | 76.6 ms                                                | 85.5 ms: 1.12x slower                                            |
| xml_etree_generate         | 85.2 ms                                                | 95.3 ms: 1.12x slower                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 77.1 ms: 1.13x slower                                            |
| regex_dna                  | 168 ms                                                 | 189 ms: 1.13x slower                                             |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                            |
| sympy_expand               | 468 ms                                                 | 539 ms: 1.15x slower                                             |
| richards                   | 45.9 ms                                                | 53.0 ms: 1.15x slower                                            |
| xml_etree_process          | 59.0 ms                                                | 68.2 ms: 1.16x slower                                            |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                            |
| scimark_lu                 | 114 ms                                                 | 133 ms: 1.17x slower                                             |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                            |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.19x slower                                             |
| richards_super             | 51.9 ms                                                | 62.3 ms: 1.20x slower                                            |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.48 ms: 1.25x slower                                            |
| fannkuch                   | 372 ms                                                 | 468 ms: 1.26x slower                                             |
| json_dumps                 | 10.4 ms                                                | 13.3 ms: 1.28x slower                                            |
| create_gc_cycles           | 1.09 ms                                                | 1.44 ms: 1.32x slower                                            |
| python_startup_no_site     | 7.16 ms                                                | 9.48 ms: 1.32x slower                                            |
| telco                      | 6.53 ms                                                | 8.73 ms: 1.34x slower                                            |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                             |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                            |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                             |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                            |
| bench_thread_pool          | 941 us                                                 | 3.12 ms: 3.32x slower                                            |
| bench_mp_pool              | 10.8 ms                                                | 87.6 ms: 8.11x slower                                            |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                     |

Benchmark hidden because not significant (2): deltablue, asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250504-3.14.0a7+-aabe31d-NOGIL/bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 90.90% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x