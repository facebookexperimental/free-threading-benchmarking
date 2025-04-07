# Results vs. 3.13.0rc2

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.002x slower
- HPT reliability: 86.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 279 ms: 1.08x slower                                                 |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                               |
| html5lib       | 68.6 ms                                                                | 64.3 ms: 1.07x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 520 ms: 1.73x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 545 ms: 1.62x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.48x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 473 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.34x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.33x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                |
| pidigits       | 216 ms                                                                 | 191 ms: 1.14x faster                                                 |
| nbody          | 85.3 ms                                                                | 114 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                |
| regex_v8       | 23.2 ms                                                                | 20.6 ms: 1.13x faster                                                |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                 |
| regex_compile  | 131 ms                                                                 | 142 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 85.0 ms: 1.11x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.12 sec: 1.05x slower                                               |
| xml_etree_generate   | 85.4 ms                                                                | 92.2 ms: 1.08x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 65.9 ms: 1.11x slower                                                |
| json_loads           | 27.3 us                                                                | 30.6 us: 1.12x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 326 us: 1.12x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.3 ms: 1.16x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 54.6 ms: 1.11x slower                                                |
| django_template | 34.2 ms                                                                | 39.6 ms: 1.16x slower                                                |
| genshi_text     | 21.7 ms                                                                | 25.7 ms: 1.18x slower                                                |
| mako            | 11.2 ms                                                                | 15.0 ms: 1.34x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.86x faster                                                |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                               |
| async_tree_io_tg           | 901 ms                                                                 | 520 ms: 1.73x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 545 ms: 1.62x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.48x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.48x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 473 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.34x faster                                                 |
| deepcopy                   | 357 us                                                                 | 288 us: 1.24x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                |
| float                      | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                |
| sqlite_synth               | 2.25 us                                                                | 1.97 us: 1.14x faster                                                |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.14x faster                                                 |
| go                         | 141 ms                                                                 | 124 ms: 1.13x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.6 ms: 1.13x faster                                                |
| scimark_sor                | 134 ms                                                                 | 118 ms: 1.13x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 85.0 ms: 1.11x faster                                                |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.91 us: 1.07x faster                                                |
| html5lib                   | 68.6 ms                                                                | 64.3 ms: 1.07x faster                                                |
| deepcopy_memo              | 38.1 us                                                                | 35.7 us: 1.07x faster                                                |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 70.6 ms: 1.05x faster                                                |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.02x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 342 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.49 sec: 1.01x slower                                               |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.02x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                               |
| generators                 | 28.5 ms                                                                | 29.5 ms: 1.03x slower                                                |
| pyflate                    | 449 ms                                                                 | 466 ms: 1.04x slower                                                 |
| json                       | 4.98 ms                                                                | 5.22 ms: 1.05x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.99 ms: 1.05x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.12 sec: 1.05x slower                                               |
| telco                      | 7.77 ms                                                                | 8.19 ms: 1.05x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 764 ms: 1.06x slower                                                 |
| 2to3                       | 259 ms                                                                 | 279 ms: 1.08x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 106 ns: 1.08x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 92.2 ms: 1.08x slower                                                |
| pprint_pformat             | 1.46 sec                                                               | 1.58 sec: 1.08x slower                                               |
| regex_compile              | 131 ms                                                                 | 142 ms: 1.08x slower                                                 |
| chaos                      | 56.3 ms                                                                | 61.7 ms: 1.10x slower                                                |
| nqueens                    | 77.7 ms                                                                | 85.3 ms: 1.10x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.80 us: 1.11x slower                                                |
| xml_etree_process          | 59.2 ms                                                                | 65.9 ms: 1.11x slower                                                |
| genshi_xml                 | 49.1 ms                                                                | 54.6 ms: 1.11x slower                                                |
| hexiom                     | 5.95 ms                                                                | 6.63 ms: 1.11x slower                                                |
| json_loads                 | 27.3 us                                                                | 30.6 us: 1.12x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 326 us: 1.12x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 126 ms: 1.12x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 74.1 ms: 1.13x slower                                                |
| richards                   | 44.4 ms                                                                | 50.0 ms: 1.13x slower                                                |
| logging_format             | 6.92 us                                                                | 7.80 us: 1.13x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 22.3 ms: 1.13x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.52 ms: 1.14x slower                                                |
| richards_super             | 50.4 ms                                                                | 57.6 ms: 1.14x slower                                                |
| sympy_str                  | 274 ms                                                                 | 317 ms: 1.16x slower                                                 |
| raytrace                   | 250 ms                                                                 | 289 ms: 1.16x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 526 ms: 1.16x slower                                                 |
| django_template            | 34.2 ms                                                                | 39.6 ms: 1.16x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 179 ms: 1.16x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.3 ms: 1.16x slower                                                |
| comprehensions             | 16.6 us                                                                | 19.3 us: 1.16x slower                                                |
| genshi_text                | 21.7 ms                                                                | 25.7 ms: 1.18x slower                                                |
| fannkuch                   | 376 ms                                                                 | 454 ms: 1.21x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 83.3 ms: 1.22x slower                                                |
| typing_runtime_protocols   | 156 us                                                                 | 191 us: 1.23x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.23x slower                                                 |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.31x slower                                                 |
| nbody                      | 85.3 ms                                                                | 114 ms: 1.33x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.0 ms: 1.34x slower                                                |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                |
| bench_thread_pool          | 924 us                                                                 | 3.14 ms: 3.39x slower                                                |
| bench_mp_pool              | 11.0 ms                                                                | 94.8 ms: 8.62x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                         |

Benchmark hidden because not significant (3): pylint, pathlib, pycparser
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250407-3.14.0a6+-521fae6-NOGIL/bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 86.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x