# Results vs. 3.12.6

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.032x faster
- HPT reliability: 72.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                 |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                               |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 545 ms: 1.99x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.98x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.97x faster                                                 |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.2 ms: 1.20x faster                                                |
| pidigits       | 184 ms                                                 | 191 ms: 1.03x slower                                                 |
| nbody          | 89.3 ms                                                | 114 ms: 1.28x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.20x faster                                                |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 85.0 ms: 1.14x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 2.12 sec: 1.01x slower                                               |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 326 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 92.2 ms: 1.08x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 65.9 ms: 1.12x slower                                                |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                                |
| json_dumps           | 10.4 ms                                                | 12.3 ms: 1.19x slower                                                |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.56x slower                                                |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.6 ms: 1.09x slower                                                |
| genshi_text     | 22.8 ms                                                | 25.7 ms: 1.13x slower                                                |
| django_template | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                |
| mako            | 11.0 ms                                                | 15.0 ms: 1.37x slower                                                |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 545 ms: 1.99x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.98x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.97x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                               |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                 |
| deepcopy                   | 352 us                                                 | 288 us: 1.22x faster                                                 |
| float                      | 80.8 ms                                                | 67.2 ms: 1.20x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.20x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 85.0 ms: 1.14x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 35.7 us: 1.13x faster                                                |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                |
| sqlite_synth               | 2.20 us                                                | 1.97 us: 1.12x faster                                                |
| scimark_sor                | 130 ms                                                 | 118 ms: 1.10x faster                                                 |
| generators                 | 32.2 ms                                                | 29.5 ms: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.91 us: 1.06x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.49 sec: 1.05x faster                                               |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.05x faster                                                 |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                               |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                 |
| raytrace                   | 299 ms                                                 | 289 ms: 1.03x faster                                                 |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                 |
| comprehensions             | 19.8 us                                                | 19.3 us: 1.03x faster                                                |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 2.12 sec: 1.01x slower                                               |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                               |
| deltablue                  | 3.45 ms                                                | 3.52 ms: 1.02x slower                                                |
| logging_simple             | 6.63 us                                                | 6.80 us: 1.03x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 764 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                 |
| pidigits                   | 184 ms                                                 | 191 ms: 1.03x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.58 sec: 1.04x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                                 |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                 |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 326 us: 1.06x slower                                                 |
| logging_format             | 7.35 us                                                | 7.80 us: 1.06x slower                                                |
| nqueens                    | 80.1 ms                                                | 85.3 ms: 1.06x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.63 ms: 1.07x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 92.2 ms: 1.08x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 74.1 ms: 1.08x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 22.3 ms: 1.08x slower                                                |
| sympy_str                  | 292 ms                                                 | 317 ms: 1.09x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 83.3 ms: 1.09x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 54.6 ms: 1.09x slower                                                |
| richards                   | 45.9 ms                                                | 50.0 ms: 1.09x slower                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.0 ms: 1.10x slower                                                |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.10x slower                                                 |
| richards_super             | 51.9 ms                                                | 57.6 ms: 1.11x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 65.9 ms: 1.12x slower                                                |
| sympy_expand               | 468 ms                                                 | 526 ms: 1.12x slower                                                 |
| genshi_text                | 22.8 ms                                                | 25.7 ms: 1.13x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.99 ms: 1.14x slower                                                |
| django_template            | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.3 ms: 1.19x slower                                                |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                |
| telco                      | 6.53 ms                                                | 8.19 ms: 1.25x slower                                                |
| nbody                      | 89.3 ms                                                | 114 ms: 1.28x slower                                                 |
| mako                       | 11.0 ms                                                | 15.0 ms: 1.37x slower                                                |
| coverage                   | 71.4 ms                                                | 108 ms: 1.51x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.56x slower                                                |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.14 ms: 3.33x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 94.8 ms: 8.78x slower                                                |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (4): regex_v8, regex_compile, scimark_fft, html5lib
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-521fae6-NOGIL/bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 72.11% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x