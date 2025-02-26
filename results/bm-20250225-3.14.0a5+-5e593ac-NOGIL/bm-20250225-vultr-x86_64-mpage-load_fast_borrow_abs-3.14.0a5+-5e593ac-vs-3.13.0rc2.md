# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 5e593ac
- commit date: 2025-02-25
- overall geometric mean: 1.048x slower
- HPT reliability: 99.90%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 71.0 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 539 ms: 1.67x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 570 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.44x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 484 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 515 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                  |
| float          | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                                 |
| nbody          | 85.3 ms                                                                | 117 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| regex_dna      | 189 ms                                                                 | 186 ms: 1.01x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| json_loads           | 27.3 us                                                                | 30.3 us: 1.11x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.28 sec: 1.13x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 237 us: 1.14x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.2 ms: 1.15x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 345 us: 1.18x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.3 ms: 1.19x slower                                                 |
| django_template | 34.2 ms                                                                | 41.2 ms: 1.21x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.0 ms: 1.24x slower                                                 |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 539 ms: 1.67x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 570 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.44x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 484 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 515 ms: 1.29x faster                                                  |
| deepcopy                   | 357 us                                                                 | 295 us: 1.21x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                  |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                                  |
| float                      | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.07 us: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.1 us: 1.05x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 128 ms: 1.05x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.03x faster                                                  |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.07 us: 1.02x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 186 ms: 1.01x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 344 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 71.0 ms: 1.03x slower                                                 |
| pyflate                    | 449 ms                                                                 | 465 ms: 1.04x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.62 sec: 1.04x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.04x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                |
| json                       | 4.98 ms                                                                | 5.24 ms: 1.05x slower                                                 |
| regex_v8                   | 23.2 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 106 ns: 1.08x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.44 ms: 1.09x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.55 sec: 1.09x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.22 ms: 1.10x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.3 us: 1.11x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 798 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                 |
| dulwich_log                | 74.5 ms                                                                | 83.0 ms: 1.11x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 118 ms: 1.12x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.64 sec: 1.12x slower                                                |
| thrift                     | 772 us                                                                 | 870 us: 1.13x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.28 sec: 1.13x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 237 us: 1.14x slower                                                  |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.01 us: 1.14x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 60.2 ms: 1.14x slower                                                 |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 68.2 ms: 1.15x slower                                                 |
| generators                 | 28.5 ms                                                                | 32.9 ms: 1.15x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.01 us: 1.16x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.3 ms: 1.16x slower                                                 |
| chaos                      | 56.3 ms                                                                | 65.4 ms: 1.16x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.60 ms: 1.16x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.3 us: 1.17x slower                                                 |
| coverage                   | 82.5 ms                                                                | 96.2 ms: 1.17x slower                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.82 ms: 1.17x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 345 us: 1.18x slower                                                  |
| richards                   | 44.4 ms                                                                | 52.7 ms: 1.19x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 58.3 ms: 1.19x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 134 ms: 1.19x slower                                                  |
| raytrace                   | 250 ms                                                                 | 299 ms: 1.20x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.6 ms: 1.20x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.14 ms: 1.20x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 545 ms: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.50 ms: 1.20x slower                                                 |
| django_template            | 34.2 ms                                                                | 41.2 ms: 1.21x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                                  |
| richards_super             | 50.4 ms                                                                | 61.3 ms: 1.22x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 95.3 ms: 1.23x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 464 ms: 1.23x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 84.4 ms: 1.24x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 27.0 ms: 1.24x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                 |
| nbody                      | 85.3 ms                                                                | 117 ms: 1.37x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.29 ms: 3.55x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.8 ms: 8.62x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.90% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x