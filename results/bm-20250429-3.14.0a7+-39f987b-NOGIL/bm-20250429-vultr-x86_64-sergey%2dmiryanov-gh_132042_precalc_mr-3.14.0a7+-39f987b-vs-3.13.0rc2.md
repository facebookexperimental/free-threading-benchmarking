# Results vs. 3.13.0rc2

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.003x slower
- HPT reliability: 85.10%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 279 ms: 1.07x slower                                                              |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                            |
| html5lib       | 68.6 ms                                                                | 65.3 ms: 1.05x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 526 ms: 1.71x faster                                                              |
| async_tree_io              | 881 ms                                                                 | 550 ms: 1.60x faster                                                              |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.47x faster                                                              |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.47x faster                                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                              |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                                              |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                                              |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                                      |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 66.8 ms: 1.15x faster                                                             |
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                                              |
| nbody          | 85.3 ms                                                                | 110 ms: 1.29x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                             |
| regex_v8       | 23.2 ms                                                                | 20.3 ms: 1.14x faster                                                             |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                              |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.09x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                             |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                              |
| tomli_loads          | 2.01 sec                                                               | 2.09 sec: 1.04x slower                                                            |
| xml_etree_generate   | 85.4 ms                                                                | 92.7 ms: 1.08x slower                                                             |
| unpickle_pure_python | 208 us                                                                 | 226 us: 1.09x slower                                                              |
| json_loads           | 27.3 us                                                                | 30.1 us: 1.10x slower                                                             |
| xml_etree_process    | 59.2 ms                                                                | 66.1 ms: 1.12x slower                                                             |
| pickle_pure_python   | 292 us                                                                 | 327 us: 1.12x slower                                                              |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.19 ms: 1.24x slower                                                             |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.39x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.31x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.1 ms: 1.12x slower                                                             |
| django_template | 34.2 ms                                                                | 39.7 ms: 1.16x slower                                                             |
| genshi_text     | 21.7 ms                                                                | 26.0 ms: 1.19x slower                                                             |
| mako            | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                             |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                                             |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.80x faster                                                            |
| async_tree_io_tg           | 901 ms                                                                 | 526 ms: 1.71x faster                                                              |
| async_tree_io              | 881 ms                                                                 | 550 ms: 1.60x faster                                                              |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.47x faster                                                              |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.47x faster                                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                              |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                                              |
| deepcopy                   | 357 us                                                                 | 291 us: 1.23x faster                                                              |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                             |
| float                      | 76.7 ms                                                                | 66.8 ms: 1.15x faster                                                             |
| regex_v8                   | 23.2 ms                                                                | 20.3 ms: 1.14x faster                                                             |
| scimark_sor                | 134 ms                                                                 | 118 ms: 1.13x faster                                                              |
| go                         | 141 ms                                                                 | 125 ms: 1.13x faster                                                              |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                             |
| deepcopy_memo              | 38.1 us                                                                | 34.5 us: 1.10x faster                                                             |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                                              |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                             |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                              |
| dulwich_log                | 74.5 ms                                                                | 70.5 ms: 1.06x faster                                                             |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                              |
| html5lib                   | 68.6 ms                                                                | 65.3 ms: 1.05x faster                                                             |
| deepcopy_reduce            | 3.12 us                                                                | 2.99 us: 1.04x faster                                                             |
| spectral_norm              | 108 ms                                                                 | 104 ms: 1.04x faster                                                              |
| scimark_fft                | 348 ms                                                                 | 338 ms: 1.03x faster                                                              |
| bpe_tokeniser              | 4.46 sec                                                               | 4.37 sec: 1.02x faster                                                            |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                                              |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                            |
| pyflate                    | 449 ms                                                                 | 455 ms: 1.01x slower                                                              |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                             |
| json                       | 4.98 ms                                                                | 5.08 ms: 1.02x slower                                                             |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.90 ms: 1.03x slower                                                             |
| tomli_loads                | 2.01 sec                                                               | 2.09 sec: 1.04x slower                                                            |
| logging_silent             | 98.2 ns                                                                | 105 ns: 1.07x slower                                                              |
| 2to3                       | 259 ms                                                                 | 279 ms: 1.07x slower                                                              |
| telco                      | 7.77 ms                                                                | 8.36 ms: 1.08x slower                                                             |
| chaos                      | 56.3 ms                                                                | 60.6 ms: 1.08x slower                                                             |
| pprint_safe_repr           | 719 ms                                                                 | 774 ms: 1.08x slower                                                              |
| generators                 | 28.5 ms                                                                | 30.8 ms: 1.08x slower                                                             |
| xml_etree_generate         | 85.4 ms                                                                | 92.7 ms: 1.08x slower                                                             |
| unpickle_pure_python       | 208 us                                                                 | 226 us: 1.09x slower                                                              |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.09x slower                                                              |
| nqueens                    | 77.7 ms                                                                | 85.4 ms: 1.10x slower                                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.60 sec: 1.10x slower                                                            |
| json_loads                 | 27.3 us                                                                | 30.1 us: 1.10x slower                                                             |
| richards                   | 44.4 ms                                                                | 49.5 ms: 1.12x slower                                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.4 ms: 1.12x slower                                                             |
| xml_etree_process          | 59.2 ms                                                                | 66.1 ms: 1.12x slower                                                             |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                             |
| pickle_pure_python         | 292 us                                                                 | 327 us: 1.12x slower                                                              |
| genshi_xml                 | 49.1 ms                                                                | 55.1 ms: 1.12x slower                                                             |
| hexiom                     | 5.95 ms                                                                | 6.71 ms: 1.13x slower                                                             |
| richards_super             | 50.4 ms                                                                | 57.4 ms: 1.14x slower                                                             |
| deltablue                  | 3.10 ms                                                                | 3.53 ms: 1.14x slower                                                             |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                              |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                              |
| raytrace                   | 250 ms                                                                 | 288 ms: 1.15x slower                                                              |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                                              |
| django_template            | 34.2 ms                                                                | 39.7 ms: 1.16x slower                                                             |
| logging_simple             | 6.14 us                                                                | 7.14 us: 1.16x slower                                                             |
| logging_format             | 6.92 us                                                                | 8.07 us: 1.17x slower                                                             |
| sympy_expand               | 454 ms                                                                 | 530 ms: 1.17x slower                                                              |
| comprehensions             | 16.6 us                                                                | 19.4 us: 1.17x slower                                                             |
| genshi_text                | 21.7 ms                                                                | 26.0 ms: 1.19x slower                                                             |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                             |
| fannkuch                   | 376 ms                                                                 | 454 ms: 1.21x slower                                                              |
| crypto_pyaes               | 68.2 ms                                                                | 82.6 ms: 1.21x slower                                                             |
| typing_runtime_protocols   | 156 us                                                                 | 191 us: 1.23x slower                                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.19 ms: 1.24x slower                                                             |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.26x slower                                                              |
| nbody                      | 85.3 ms                                                                | 110 ms: 1.29x slower                                                              |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                              |
| mako                       | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                             |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.39x slower                                                             |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                                             |
| bench_mp_pool              | 11.0 ms                                                                | 94.1 ms: 8.56x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                                      |

Benchmark hidden because not significant (4): pylint, pathlib, asyncio_websockets, coroutines
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 85.10% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x