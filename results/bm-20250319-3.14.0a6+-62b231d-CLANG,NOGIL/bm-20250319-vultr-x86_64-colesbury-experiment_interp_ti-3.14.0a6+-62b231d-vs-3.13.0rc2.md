# Results vs. 3.13.0rc2

- fork: colesbury
- ref: experiment_interp_ti
- machine: linux-x86_64
- commit hash: 62b231d
- commit date: 2025-03-19
- overall geometric mean: 1.009x faster
- HPT reliability: 88.47%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 276 ms: 1.06x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 68.6 ms                                                                | 63.3 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 493 ms: 1.83x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 529 ms: 1.67x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 213 ms: 1.57x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 274 ms: 1.50x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 435 ms: 1.46x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 469 ms: 1.42x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 252 ms: 1.40x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 19.5 ms: 1.20x faster                                                     |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                      |
| Geometric mean             | (ref)                                                                  | 1.41x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                      |
| float          | 76.7 ms                                                                | 69.1 ms: 1.11x faster                                                     |
| nbody          | 85.3 ms                                                                | 120 ms: 1.40x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                     |
| regex_effbot   | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                     |
| regex_dna      | 189 ms                                                                 | 188 ms: 1.01x faster                                                      |
| regex_compile  | 131 ms                                                                 | 140 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.0 ms: 1.10x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 85.6 ms: 1.00x slower                                                     |
| xml_etree_process    | 59.2 ms                                                                | 60.9 ms: 1.03x slower                                                     |
| tomli_loads          | 2.01 sec                                                               | 2.11 sec: 1.05x slower                                                    |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| unpickle_pure_python | 208 us                                                                 | 227 us: 1.09x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 321 us: 1.10x slower                                                      |
| json_loads           | 27.3 us                                                                | 30.2 us: 1.11x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                     |
| python_startup_no_site | 7.41 ms                                                                | 11.0 ms: 1.49x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.45x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 52.1 ms: 1.06x slower                                                     |
| django_template | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                                     |
| genshi_text     | 21.7 ms                                                                | 24.4 ms: 1.12x slower                                                     |
| mako            | 11.2 ms                                                                | 14.9 ms: 1.33x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.15x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 493 ms: 1.83x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 529 ms: 1.67x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 2.07 ms: 1.60x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 213 ms: 1.57x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 274 ms: 1.50x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 435 ms: 1.46x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 469 ms: 1.42x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 252 ms: 1.40x faster                                                      |
| deepcopy                   | 357 us                                                                 | 268 us: 1.33x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 19.5 ms: 1.20x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 113 ms: 1.18x faster                                                      |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                      |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                      |
| go                         | 141 ms                                                                 | 124 ms: 1.14x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.75 us: 1.14x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 1.99 us: 1.13x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 95.2 ms: 1.13x faster                                                     |
| float                      | 76.7 ms                                                                | 69.1 ms: 1.11x faster                                                     |
| deepcopy_memo              | 38.1 us                                                                | 34.4 us: 1.11x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 89.3 ns: 1.10x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.0 ms: 1.10x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 63.3 ms: 1.08x faster                                                     |
| pylint                     | 317 ms                                                                 | 294 ms: 1.08x faster                                                      |
| regex_v8                   | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 70.9 ms: 1.05x faster                                                     |
| generators                 | 28.5 ms                                                                | 27.4 ms: 1.04x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.01x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.01x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 345 ms: 1.01x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 188 ms: 1.01x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 85.6 ms: 1.00x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 60.9 ms: 1.03x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.03x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 117 ms: 1.04x slower                                                      |
| telco                      | 7.77 ms                                                                | 8.08 ms: 1.04x slower                                                     |
| json                       | 4.98 ms                                                                | 5.20 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.96 ms: 1.04x slower                                                     |
| richards                   | 44.4 ms                                                                | 46.6 ms: 1.05x slower                                                     |
| tomli_loads                | 2.01 sec                                                               | 2.11 sec: 1.05x slower                                                    |
| logging_simple             | 6.14 us                                                                | 6.46 us: 1.05x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| logging_format             | 6.92 us                                                                | 7.29 us: 1.05x slower                                                     |
| genshi_xml                 | 49.1 ms                                                                | 52.1 ms: 1.06x slower                                                     |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                                     |
| 2to3                       | 259 ms                                                                 | 276 ms: 1.06x slower                                                      |
| regex_compile              | 131 ms                                                                 | 140 ms: 1.07x slower                                                      |
| thrift                     | 772 us                                                                 | 827 us: 1.07x slower                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 70.8 ms: 1.08x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 781 ms: 1.09x slower                                                      |
| django_template            | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                                     |
| chaos                      | 56.3 ms                                                                | 61.2 ms: 1.09x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 227 us: 1.09x slower                                                      |
| nqueens                    | 77.7 ms                                                                | 84.9 ms: 1.09x slower                                                     |
| coverage                   | 82.5 ms                                                                | 90.4 ms: 1.10x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 321 us: 1.10x slower                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.60 sec: 1.10x slower                                                    |
| richards_super             | 50.4 ms                                                                | 55.6 ms: 1.10x slower                                                     |
| json_loads                 | 27.3 us                                                                | 30.2 us: 1.11x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 6.58 ms: 1.11x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 505 ms: 1.11x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 172 ms: 1.12x slower                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 174 us: 1.12x slower                                                      |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 308 ms: 1.12x slower                                                      |
| genshi_text                | 21.7 ms                                                                | 24.4 ms: 1.12x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.55 ms: 1.15x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 433 ms: 1.15x slower                                                      |
| raytrace                   | 250 ms                                                                 | 288 ms: 1.15x slower                                                      |
| meteor_contest             | 101 ms                                                                 | 120 ms: 1.19x slower                                                      |
| crypto_pyaes               | 68.2 ms                                                                | 80.9 ms: 1.19x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                     |
| mdp                        | 2.34 sec                                                               | 2.80 sec: 1.20x slower                                                    |
| mako                       | 11.2 ms                                                                | 14.9 ms: 1.33x slower                                                     |
| nbody                      | 85.3 ms                                                                | 120 ms: 1.40x slower                                                      |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 11.0 ms: 1.49x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.12 ms: 3.37x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 95.4 ms: 8.67x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (2): asyncio_websockets, pyflate
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250319-3.14.0a6+-62b231d-CLANG,NOGIL/bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 88.47% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x