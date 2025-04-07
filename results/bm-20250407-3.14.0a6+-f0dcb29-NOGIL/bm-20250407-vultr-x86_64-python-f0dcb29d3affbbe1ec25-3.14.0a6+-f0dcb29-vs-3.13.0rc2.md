# Results vs. 3.13.0rc2

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.106x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 310 ms: 1.19x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.91 sec: 1.11x slower                                                 |
| html5lib       | 68.6 ms                                                                | 75.8 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 567 ms: 1.59x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 597 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 246 ms: 1.36x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 339 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 312 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 498 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 525 ms: 1.27x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 280 ms: 1.26x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                   |
| async_generators           | 375 ms                                                                 | 387 ms: 1.03x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 27.0 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| float          | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                                  |
| nbody          | 85.3 ms                                                                | 140 ms: 1.64x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.96 ms: 1.09x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                  |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                                   |
| regex_compile  | 131 ms                                                                 | 169 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.1 ms: 1.01x faster                                                  |
| json_loads           | 27.3 us                                                                | 30.3 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.19x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 13.2 ms: 1.24x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.51 sec: 1.25x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 74.2 ms: 1.25x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 270 us: 1.30x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 381 us: 1.31x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.17x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 45.1 ms: 1.32x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 68.4 ms: 1.39x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 31.4 ms: 1.45x slower                                                  |
| mako            | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.87x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.47 sec: 1.59x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 567 ms: 1.59x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 597 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 246 ms: 1.36x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 339 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 312 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 498 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 525 ms: 1.27x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 280 ms: 1.26x faster                                                   |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| deepcopy                   | 357 us                                                                 | 327 us: 1.09x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.06 us: 1.09x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.96 ms: 1.09x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.1 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                   |
| float                      | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                                  |
| json                       | 4.98 ms                                                                | 5.11 ms: 1.02x slower                                                  |
| async_generators           | 375 ms                                                                 | 387 ms: 1.03x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 19.9 ms: 1.03x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.27 us: 1.05x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 78.3 ms: 1.05x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 40.2 us: 1.06x slower                                                  |
| go                         | 141 ms                                                                 | 153 ms: 1.09x slower                                                   |
| scimark_fft                | 348 ms                                                                 | 379 ms: 1.09x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 118 ms: 1.10x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 75.8 ms: 1.11x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.91 sec: 1.11x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.3 us: 1.11x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.94 sec: 1.11x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.64 ms: 1.11x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.25 sec: 1.11x slower                                                 |
| scimark_sor                | 134 ms                                                                 | 151 ms: 1.13x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 27.0 ms: 1.16x slower                                                  |
| pyflate                    | 449 ms                                                                 | 529 ms: 1.18x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.59 ms: 1.18x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.19x slower                                                   |
| 2to3                       | 259 ms                                                                 | 310 ms: 1.19x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.2 ms: 1.23x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 890 ms: 1.24x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 13.2 ms: 1.24x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.51 sec: 1.25x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 74.2 ms: 1.25x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.26x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 195 ms: 1.27x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 124 ns: 1.27x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.85 sec: 1.27x slower                                                 |
| chaos                      | 56.3 ms                                                                | 71.8 ms: 1.27x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 352 ms: 1.28x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 584 ms: 1.29x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 100 ms: 1.29x slower                                                   |
| regex_compile              | 131 ms                                                                 | 169 ms: 1.29x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 270 us: 1.30x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 381 us: 1.31x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 86.4 ms: 1.31x slower                                                  |
| django_template            | 34.2 ms                                                                | 45.1 ms: 1.32x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 206 us: 1.33x slower                                                   |
| comprehensions             | 16.6 us                                                                | 22.0 us: 1.33x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 90.9 ms: 1.33x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 136 ms: 1.34x slower                                                   |
| coverage                   | 82.5 ms                                                                | 111 ms: 1.34x slower                                                   |
| richards                   | 44.4 ms                                                                | 59.8 ms: 1.35x slower                                                  |
| richards_super             | 50.4 ms                                                                | 68.3 ms: 1.35x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 8.08 ms: 1.36x slower                                                  |
| raytrace                   | 250 ms                                                                 | 341 ms: 1.36x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 514 ms: 1.37x slower                                                   |
| logging_simple             | 6.14 us                                                                | 8.42 us: 1.37x slower                                                  |
| logging_format             | 6.92 us                                                                | 9.56 us: 1.38x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 68.4 ms: 1.39x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 4.45 ms: 1.44x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 31.4 ms: 1.45x slower                                                  |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                  |
| mako                       | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| generators                 | 28.5 ms                                                                | 44.5 ms: 1.56x slower                                                  |
| nbody                      | 85.3 ms                                                                | 140 ms: 1.64x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.18 ms: 3.44x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 97.4 ms: 8.85x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                           |

Benchmark hidden because not significant (2): create_gc_cycles, pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.106x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.36x