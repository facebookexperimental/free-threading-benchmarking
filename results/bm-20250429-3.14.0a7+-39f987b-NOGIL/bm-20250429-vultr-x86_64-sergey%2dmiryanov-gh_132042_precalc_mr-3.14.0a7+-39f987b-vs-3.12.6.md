# Results vs. 3.12.6

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.031x faster
- HPT reliability: 62.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                              |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                            |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 526 ms: 2.11x faster                                                              |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                              |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                              |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                              |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                              |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                              |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 66.8 ms: 1.21x faster                                                             |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                                              |
| nbody          | 89.3 ms                                                | 110 ms: 1.23x slower                                                              |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                             |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                             |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                              |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                              |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                             |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                              |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                            |
| unpickle_pure_python | 221 us                                                 | 226 us: 1.03x slower                                                              |
| pickle_pure_python   | 308 us                                                 | 327 us: 1.06x slower                                                              |
| xml_etree_generate   | 85.2 ms                                                | 92.7 ms: 1.09x slower                                                             |
| xml_etree_process    | 59.0 ms                                                | 66.1 ms: 1.12x slower                                                             |
| json_loads           | 26.5 us                                                | 30.1 us: 1.14x slower                                                             |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.19 ms: 1.28x slower                                                             |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                             |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                             |
| genshi_text     | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                             |
| django_template | 34.7 ms                                                | 39.7 ms: 1.14x slower                                                             |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                             |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 526 ms: 2.11x faster                                                              |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                              |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                              |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                             |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                            |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                              |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                              |
| float                      | 80.8 ms                                                | 66.8 ms: 1.21x faster                                                             |
| deepcopy                   | 352 us                                                 | 291 us: 1.21x faster                                                              |
| deepcopy_memo              | 40.3 us                                                | 34.5 us: 1.17x faster                                                             |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                             |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                             |
| dulwich_log                | 78.9 ms                                                | 70.5 ms: 1.12x faster                                                             |
| go                         | 139 ms                                                 | 125 ms: 1.12x faster                                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                             |
| scimark_sor                | 130 ms                                                 | 118 ms: 1.10x faster                                                              |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                              |
| spectral_norm              | 110 ms                                                 | 104 ms: 1.06x faster                                                              |
| generators                 | 32.2 ms                                                | 30.8 ms: 1.05x faster                                                             |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                              |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                              |
| raytrace                   | 299 ms                                                 | 288 ms: 1.04x faster                                                              |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                              |
| chaos                      | 62.8 ms                                                | 60.6 ms: 1.04x faster                                                             |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.99 us: 1.03x faster                                                             |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                                             |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                             |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                             |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                              |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                            |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                              |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                             |
| pyflate                    | 448 ms                                                 | 455 ms: 1.02x slower                                                              |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                            |
| deltablue                  | 3.45 ms                                                | 3.53 ms: 1.02x slower                                                             |
| unpickle_pure_python       | 221 us                                                 | 226 us: 1.03x slower                                                              |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                             |
| pprint_safe_repr           | 743 ms                                                 | 774 ms: 1.04x slower                                                              |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                              |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.05x slower                                                            |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                              |
| pickle_pure_python         | 308 us                                                 | 327 us: 1.06x slower                                                              |
| nqueens                    | 80.1 ms                                                | 85.4 ms: 1.07x slower                                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.4 ms: 1.07x slower                                                             |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 73.4 ms: 1.07x slower                                                             |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                             |
| logging_simple             | 6.63 us                                                | 7.14 us: 1.08x slower                                                             |
| richards                   | 45.9 ms                                                | 49.5 ms: 1.08x slower                                                             |
| crypto_pyaes               | 76.6 ms                                                | 82.6 ms: 1.08x slower                                                             |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                              |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                                              |
| xml_etree_generate         | 85.2 ms                                                | 92.7 ms: 1.09x slower                                                             |
| hexiom                     | 6.17 ms                                                | 6.71 ms: 1.09x slower                                                             |
| genshi_xml                 | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                             |
| logging_format             | 7.35 us                                                | 8.07 us: 1.10x slower                                                             |
| richards_super             | 51.9 ms                                                | 57.4 ms: 1.11x slower                                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.90 ms: 1.12x slower                                                             |
| xml_etree_process          | 59.0 ms                                                | 66.1 ms: 1.12x slower                                                             |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                              |
| sympy_expand               | 468 ms                                                 | 530 ms: 1.13x slower                                                              |
| json_loads                 | 26.5 us                                                | 30.1 us: 1.14x slower                                                             |
| genshi_text                | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                             |
| django_template            | 34.7 ms                                                | 39.7 ms: 1.14x slower                                                             |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                              |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                              |
| nbody                      | 89.3 ms                                                | 110 ms: 1.23x slower                                                              |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                             |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                             |
| telco                      | 6.53 ms                                                | 8.36 ms: 1.28x slower                                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.19 ms: 1.28x slower                                                             |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                             |
| coverage                   | 71.4 ms                                                | 109 ms: 1.53x slower                                                              |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                             |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                                             |
| bench_mp_pool              | 10.8 ms                                                | 94.1 ms: 8.72x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 62.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x