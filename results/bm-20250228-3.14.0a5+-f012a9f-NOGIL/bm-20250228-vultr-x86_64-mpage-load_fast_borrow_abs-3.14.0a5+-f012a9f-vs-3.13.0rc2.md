# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: f012a9f
- commit date: 2025-02-28
- overall geometric mean: 1.049x slower
- HPT reliability: 99.90%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                |
| html5lib       | 68.6 ms                                                                | 71.6 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 537 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 572 ms: 1.54x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 229 ms: 1.45x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.9 ms: 1.10x faster                                                 |
| pidigits       | 216 ms                                                                 | 198 ms: 1.10x faster                                                  |
| nbody          | 85.3 ms                                                                | 119 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 24.3 ms: 1.05x slower                                                 |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 234 us: 1.13x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 344 us: 1.18x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.67 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.4 ms: 1.17x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                 |
| django_template | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                 |
| mako            | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 537 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 572 ms: 1.54x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 229 ms: 1.45x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| deepcopy                   | 357 us                                                                 | 293 us: 1.22x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                 |
| float                      | 76.7 ms                                                                | 69.9 ms: 1.10x faster                                                 |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.10x faster                                                  |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 35.4 us: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 126 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.02 us: 1.03x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.03x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 342 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                                  |
| json                       | 4.98 ms                                                                | 5.04 ms: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.60 sec: 1.03x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.04x slower                                                |
| html5lib                   | 68.6 ms                                                                | 71.6 ms: 1.04x slower                                                 |
| regex_v8                   | 23.2 ms                                                                | 24.3 ms: 1.05x slower                                                 |
| pyflate                    | 449 ms                                                                 | 474 ms: 1.05x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.39 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.15 ms: 1.08x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 107 ns: 1.09x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 793 ms: 1.10x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 82.8 ms: 1.11x slower                                                 |
| thrift                     | 772 us                                                                 | 859 us: 1.11x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.64 sec: 1.12x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 234 us: 1.13x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 119 ms: 1.13x slower                                                  |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.14x slower                                                  |
| generators                 | 28.5 ms                                                                | 32.7 ms: 1.14x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 60.4 ms: 1.15x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.2 us: 1.16x slower                                                 |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.4 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.61 ms: 1.17x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.4 ms: 1.17x slower                                                 |
| chaos                      | 56.3 ms                                                                | 65.9 ms: 1.17x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.22 us: 1.18x slower                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.83 ms: 1.18x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 344 us: 1.18x slower                                                  |
| coverage                   | 82.5 ms                                                                | 97.5 ms: 1.18x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.20 us: 1.19x slower                                                 |
| richards                   | 44.4 ms                                                                | 52.8 ms: 1.19x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.10 ms: 1.19x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.6 ms: 1.20x slower                                                 |
| raytrace                   | 250 ms                                                                 | 299 ms: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 331 ms: 1.21x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 94.0 ms: 1.21x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.51 ms: 1.21x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 551 ms: 1.21x slower                                                  |
| richards_super             | 50.4 ms                                                                | 61.2 ms: 1.21x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 137 ms: 1.22x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 462 ms: 1.23x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 192 us: 1.23x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.0 ms: 1.25x slower                                                 |
| django_template            | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.67 ms: 1.30x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                 |
| nbody                      | 85.3 ms                                                                | 119 ms: 1.39x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.29 ms: 3.55x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.64x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (4): spectral_norm, pylint, create_gc_cycles, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250228-3.14.0a5+-f012a9f-NOGIL/bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.049x slower

# HPT report

- Reliability score: 99.90% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x