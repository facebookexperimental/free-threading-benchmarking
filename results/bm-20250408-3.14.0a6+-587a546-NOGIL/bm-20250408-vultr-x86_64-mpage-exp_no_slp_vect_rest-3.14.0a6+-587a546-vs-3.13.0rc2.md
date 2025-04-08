# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vect_rest
- machine: linux-x86_64
- commit hash: 587a546
- commit date: 2025-04-08
- overall geometric mean: 1.047x slower
- HPT reliability: 99.48%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                |
| html5lib       | 68.6 ms                                                                | 70.9 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 545 ms: 1.65x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 573 ms: 1.54x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.41x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 328 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 300 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 517 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 189 ms: 1.15x faster                                                  |
| float          | 76.7 ms                                                                | 70.8 ms: 1.08x faster                                                 |
| nbody          | 85.3 ms                                                                | 119 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.10x faster                                                 |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                                  |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.2 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                                |
| xml_etree_process    | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 248 us: 1.19x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 349 us: 1.20x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.52x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.48x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.5 ms: 1.23x slower                                                 |
| django_template | 34.2 ms                                                                | 42.2 ms: 1.23x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 28.5 ms: 1.31x slower                                                 |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.80 ms: 1.85x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.37 sec: 1.70x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 545 ms: 1.65x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 573 ms: 1.54x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.41x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 328 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 300 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 517 ms: 1.29x faster                                                  |
| deepcopy                   | 357 us                                                                 | 300 us: 1.19x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                                 |
| pidigits                   | 216 ms                                                                 | 189 ms: 1.15x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.10x faster                                                 |
| float                      | 76.7 ms                                                                | 70.8 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.2 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.02 us: 1.03x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 130 ms: 1.03x faster                                                  |
| go                         | 141 ms                                                                 | 137 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 73.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.01x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 357 ms: 1.02x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 70.9 ms: 1.03x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.67 sec: 1.05x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                                 |
| pyflate                    | 449 ms                                                                 | 485 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.15 ms: 1.09x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.48 ms: 1.09x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                                 |
| 2to3                       | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 814 ms: 1.13x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                                |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                  |
| chaos                      | 56.3 ms                                                                | 65.6 ms: 1.17x slower                                                 |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.17x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.1 ms: 1.17x slower                                                 |
| generators                 | 28.5 ms                                                                | 33.4 ms: 1.17x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.71 sec: 1.17x slower                                                |
| nqueens                    | 77.7 ms                                                                | 91.8 ms: 1.18x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.3 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 134 ms: 1.19x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 248 us: 1.19x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.35 us: 1.20x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 349 us: 1.20x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.31 us: 1.20x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 547 ms: 1.21x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.31 ms: 1.23x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 60.5 ms: 1.23x slower                                                 |
| django_template            | 34.2 ms                                                                | 42.2 ms: 1.23x slower                                                 |
| richards                   | 44.4 ms                                                                | 55.1 ms: 1.24x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.85 ms: 1.24x slower                                                 |
| raytrace                   | 250 ms                                                                 | 311 ms: 1.25x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 472 ms: 1.26x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.26x slower                                                  |
| comprehensions             | 16.6 us                                                                | 20.9 us: 1.26x slower                                                 |
| richards_super             | 50.4 ms                                                                | 63.5 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.26x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 86.2 ms: 1.26x slower                                                 |
| coverage                   | 82.5 ms                                                                | 107 ms: 1.30x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 28.5 ms: 1.31x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| nbody                      | 85.3 ms                                                                | 119 ms: 1.39x slower                                                  |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.52x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.41x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 96.4 ms: 8.76x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (2): deepcopy_memo, pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a6+-587a546-NOGIL/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.047x slower

# HPT report

- Reliability score: 99.48% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x