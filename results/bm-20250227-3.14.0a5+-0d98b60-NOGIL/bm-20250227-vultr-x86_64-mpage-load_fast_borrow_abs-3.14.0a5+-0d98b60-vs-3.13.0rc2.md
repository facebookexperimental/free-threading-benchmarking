# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 0d98b60
- commit date: 2025-02-27
- overall geometric mean: 1.056x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 69.3 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 537 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 569 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 193 ms: 1.12x faster                                                  |
| float          | 76.7 ms                                                                | 70.4 ms: 1.09x faster                                                 |
| nbody          | 85.3 ms                                                                | 121 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.10x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.8 ms: 1.02x faster                                                 |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| json_loads           | 27.3 us                                                                | 28.9 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 235 us: 1.13x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.1 ms: 1.15x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 345 us: 1.18x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.6 ms: 1.17x slower                                                 |
| django_template | 34.2 ms                                                                | 41.5 ms: 1.21x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.7 ms: 1.23x slower                                                 |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 537 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 569 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| deepcopy                   | 357 us                                                                 | 294 us: 1.22x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| pidigits                   | 216 ms                                                                 | 193 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.10x faster                                                  |
| float                      | 76.7 ms                                                                | 70.4 ms: 1.09x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 35.0 us: 1.09x faster                                                 |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 22.8 ms: 1.02x faster                                                 |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.08 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                 |
| scimark_sor                | 134 ms                                                                 | 134 ms: 1.00x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 69.3 ms: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.63 sec: 1.04x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.04x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                                |
| pyflate                    | 449 ms                                                                 | 471 ms: 1.05x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.9 us: 1.06x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 106 ns: 1.08x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.41 ms: 1.08x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 792 ms: 1.10x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                 |
| dulwich_log                | 74.5 ms                                                                | 83.1 ms: 1.12x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.63 sec: 1.12x slower                                                |
| thrift                     | 772 us                                                                 | 865 us: 1.12x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 118 ms: 1.12x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 235 us: 1.13x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 60.0 ms: 1.14x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.67 sec: 1.14x slower                                                |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| generators                 | 28.5 ms                                                                | 32.7 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 68.1 ms: 1.15x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.99 us: 1.16x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.12 us: 1.16x slower                                                 |
| coverage                   | 82.5 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.2 us: 1.16x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.61 ms: 1.17x slower                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.82 ms: 1.17x slower                                                 |
| chaos                      | 56.3 ms                                                                | 65.8 ms: 1.17x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.6 ms: 1.17x slower                                                 |
| richards                   | 44.4 ms                                                                | 52.4 ms: 1.18x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 345 us: 1.18x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.5 ms: 1.19x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 184 ms: 1.19x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.12 ms: 1.20x slower                                                 |
| raytrace                   | 250 ms                                                                 | 300 ms: 1.20x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.50 ms: 1.20x slower                                                 |
| richards_super             | 50.4 ms                                                                | 61.0 ms: 1.21x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                                  |
| django_template            | 34.2 ms                                                                | 41.5 ms: 1.21x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 551 ms: 1.21x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.7 ms: 1.23x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 96.0 ms: 1.24x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.24x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.4 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.26x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 450 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 88.4 ms: 1.34x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 153 ms: 1.36x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 121 ms: 1.42x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 7.45 ms: 1.57x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.28 ms: 3.55x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.7 ms: 8.61x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (3): pylint, spectral_norm, json
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250227-3.14.0a5+-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.056x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x