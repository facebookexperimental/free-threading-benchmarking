# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.053x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                |
| html5lib       | 68.6 ms                                                                | 71.7 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 544 ms: 1.66x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 575 ms: 1.53x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 335 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 301 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.9 ms: 1.10x faster                                                 |
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                                  |
| nbody          | 85.3 ms                                                                | 118 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                                 |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.8 us: 1.09x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 238 us: 1.14x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 345 us: 1.18x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.65 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.7 ms: 1.18x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.8 ms: 1.23x slower                                                 |
| django_template | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                                 |
| mako            | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 544 ms: 1.66x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 575 ms: 1.53x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 335 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 301 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                                 |
| deepcopy                   | 357 us                                                                 | 304 us: 1.17x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                 |
| float                      | 76.7 ms                                                                | 69.9 ms: 1.10x faster                                                 |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.1 us: 1.05x faster                                                 |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 129 ms: 1.04x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                 |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.17 us: 1.02x slower                                                 |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 356 ms: 1.02x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.61 sec: 1.03x slower                                                |
| pathlib                    | 19.3 ms                                                                | 20.1 ms: 1.04x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 71.7 ms: 1.05x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                |
| pyflate                    | 449 ms                                                                 | 478 ms: 1.06x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.16 ms: 1.09x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.8 us: 1.09x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.57 sec: 1.10x slower                                                |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 83.0 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| sqlglot_normalize          | 106 ms                                                                 | 119 ms: 1.13x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.77 ms: 1.13x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 816 ms: 1.14x slower                                                  |
| thrift                     | 772 us                                                                 | 879 us: 1.14x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 238 us: 1.14x slower                                                  |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 60.2 ms: 1.14x slower                                                 |
| generators                 | 28.5 ms                                                                | 32.8 ms: 1.15x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.0 ms: 1.15x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.15x slower                                                |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.2 us: 1.16x slower                                                 |
| coverage                   | 82.5 ms                                                                | 96.2 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.62 ms: 1.17x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.19 us: 1.17x slower                                                 |
| chaos                      | 56.3 ms                                                                | 66.2 ms: 1.18x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.7 ms: 1.18x slower                                                 |
| richards                   | 44.4 ms                                                                | 52.3 ms: 1.18x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.17 us: 1.18x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 345 us: 1.18x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.84 ms: 1.18x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 541 ms: 1.19x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.6 ms: 1.20x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 330 ms: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.18 ms: 1.21x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 94.2 ms: 1.21x slower                                                 |
| richards_super             | 50.4 ms                                                                | 61.1 ms: 1.21x slower                                                 |
| raytrace                   | 250 ms                                                                 | 303 ms: 1.21x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 137 ms: 1.22x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.52 ms: 1.22x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 26.8 ms: 1.23x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                  |
| django_template            | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 84.8 ms: 1.24x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.65 ms: 1.30x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                 |
| nbody                      | 85.3 ms                                                                | 118 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.29 ms: 3.55x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.8 ms: 8.62x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, spectral_norm
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.053x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x