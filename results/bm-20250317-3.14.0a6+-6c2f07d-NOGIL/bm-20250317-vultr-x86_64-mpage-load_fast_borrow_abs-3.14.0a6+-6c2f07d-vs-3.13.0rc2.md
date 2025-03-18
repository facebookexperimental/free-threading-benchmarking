# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 6c2f07d
- commit date: 2025-03-17
- overall geometric mean: 1.052x slower
- HPT reliability: 99.88%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                |
| html5lib       | 68.6 ms                                                                | 69.6 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 540 ms: 1.67x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 570 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 301 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 487 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                                  |
| float          | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                                 |
| nbody          | 85.3 ms                                                                | 119 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| regex_dna      | 189 ms                                                                 | 174 ms: 1.08x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                                 |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.26 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 96.6 ms: 1.13x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 239 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.4 ms: 1.17x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 343 us: 1.17x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.9 ms: 1.20x slower                                                 |
| django_template | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.6 ms: 1.27x slower                                                 |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 540 ms: 1.67x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 570 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 301 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 487 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| deepcopy                   | 357 us                                                                 | 302 us: 1.19x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.05 us: 1.10x faster                                                 |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 174 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| go                         | 141 ms                                                                 | 132 ms: 1.07x faster                                                  |
| float                      | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.3 us: 1.05x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 127 ms: 1.05x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.31 ms: 1.02x faster                                                 |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 73.7 ms: 1.01x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.05 ms: 1.01x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 69.6 ms: 1.02x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 356 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.03x slower                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.66 sec: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 105 ns: 1.07x slower                                                  |
| pyflate                    | 449 ms                                                                 | 483 ms: 1.07x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.44 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 796 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.28 ms: 1.11x slower                                                 |
| thrift                     | 772 us                                                                 | 858 us: 1.11x slower                                                  |
| 2to3                       | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 118 ms: 1.12x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.26 sec: 1.12x slower                                                |
| pprint_pformat             | 1.46 sec                                                               | 1.64 sec: 1.13x slower                                                |
| generators                 | 28.5 ms                                                                | 32.2 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 96.6 ms: 1.13x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 60.2 ms: 1.14x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 239 us: 1.15x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.69 sec: 1.15x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.59 ms: 1.16x slower                                                 |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.16x slower                                                  |
| chaos                      | 56.3 ms                                                                | 65.5 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.6 ms: 1.16x slower                                                 |
| coverage                   | 82.5 ms                                                                | 96.3 ms: 1.17x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.18 us: 1.17x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.08 us: 1.17x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.4 ms: 1.17x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 343 us: 1.17x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.83 ms: 1.18x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.19x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.1 ms: 1.20x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 58.9 ms: 1.20x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.8 ms: 1.20x slower                                                 |
| raytrace                   | 250 ms                                                                 | 301 ms: 1.21x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 548 ms: 1.21x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.51 ms: 1.21x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 333 ms: 1.21x slower                                                  |
| django_template            | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                                 |
| richards_super             | 50.4 ms                                                                | 61.7 ms: 1.22x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 95.4 ms: 1.23x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 139 ms: 1.24x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.39 ms: 1.24x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 85.2 ms: 1.25x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 470 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.27x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 27.6 ms: 1.27x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| nbody                      | 85.3 ms                                                                | 119 ms: 1.39x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 95.3 ms: 8.66x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (4): pylint, spectral_norm, deepcopy_reduce, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250317-3.14.0a6+-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.052x slower

# HPT report

- Reliability score: 99.88% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.34x