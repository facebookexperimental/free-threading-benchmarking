# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 08402c0
- commit date: 2025-02-19
- overall geometric mean: 1.024x slower
- HPT reliability: 98.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 285 ms: 1.10x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.6 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 534 ms: 1.69x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 559 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 326 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 295 ms: 1.39x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 483 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 515 ms: 1.29x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.3 ms: 1.04x faster                                                 |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.30x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.7 ms: 1.13x faster                                                 |
| pidigits       | 216 ms                                                                 | 203 ms: 1.06x faster                                                  |
| nbody          | 85.3 ms                                                                | 114 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                 |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 85.5 ms: 1.10x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 91.6 ms: 1.07x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 227 us: 1.09x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 66.1 ms: 1.12x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 330 us: 1.13x slower                                                  |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.58 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.3 ms: 1.13x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 25.8 ms: 1.19x slower                                                 |
| django_template | 34.2 ms                                                                | 41.6 ms: 1.22x slower                                                 |
| mako            | 11.2 ms                                                                | 14.8 ms: 1.32x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 534 ms: 1.69x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 559 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 326 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 295 ms: 1.39x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 483 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 515 ms: 1.29x faster                                                  |
| deepcopy                   | 357 us                                                                 | 295 us: 1.21x faster                                                  |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                 |
| float                      | 76.7 ms                                                                | 67.7 ms: 1.13x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.2 us: 1.11x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 85.5 ms: 1.10x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| pidigits                   | 216 ms                                                                 | 203 ms: 1.06x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 65.6 ms: 1.05x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.3 ms: 1.04x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.04 us: 1.03x faster                                                 |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.02x faster                                                  |
| logging_silent             | 98.2 ns                                                                | 96.7 ns: 1.02x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.42 sec: 1.01x faster                                                |
| scimark_fft                | 348 ms                                                                 | 345 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| regex_v8                   | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| pyflate                    | 449 ms                                                                 | 462 ms: 1.03x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                |
| generators                 | 28.5 ms                                                                | 29.4 ms: 1.03x slower                                                 |
| json                       | 4.98 ms                                                                | 5.30 ms: 1.06x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.08 ms: 1.07x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 770 ms: 1.07x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 91.6 ms: 1.07x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.51 sec: 1.07x slower                                                |
| dulwich_log                | 74.5 ms                                                                | 80.8 ms: 1.08x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 115 ms: 1.09x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.45 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 227 us: 1.09x slower                                                  |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.59 sec: 1.09x slower                                                |
| 2to3                       | 259 ms                                                                 | 285 ms: 1.10x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 58.4 ms: 1.11x slower                                                 |
| richards                   | 44.4 ms                                                                | 49.3 ms: 1.11x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.45 ms: 1.11x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 66.1 ms: 1.12x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.5 ms: 1.12x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.66 ms: 1.12x slower                                                 |
| comprehensions             | 16.6 us                                                                | 18.6 us: 1.12x slower                                                 |
| chaos                      | 56.3 ms                                                                | 63.2 ms: 1.12x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.90 us: 1.12x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 55.3 ms: 1.13x slower                                                 |
| thrift                     | 772 us                                                                 | 872 us: 1.13x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.81 us: 1.13x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 330 us: 1.13x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.76 ms: 1.13x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 88.8 ms: 1.14x slower                                                 |
| richards_super             | 50.4 ms                                                                | 57.8 ms: 1.15x slower                                                 |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| coverage                   | 82.5 ms                                                                | 95.3 ms: 1.16x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 526 ms: 1.16x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.0 ms: 1.17x slower                                                 |
| raytrace                   | 250 ms                                                                 | 292 ms: 1.17x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.46 ms: 1.17x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 321 ms: 1.17x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.18x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 25.8 ms: 1.19x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 453 ms: 1.21x slower                                                  |
| django_template            | 34.2 ms                                                                | 41.6 ms: 1.22x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 83.2 ms: 1.22x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 192 us: 1.23x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.58 ms: 1.29x slower                                                 |
| mako                       | 11.2 ms                                                                | 14.8 ms: 1.32x slower                                                 |
| nbody                      | 85.3 ms                                                                | 114 ms: 1.33x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.26 ms: 3.52x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.3 ms: 8.57x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-08402c0-NOGIL/bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 98.18% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x