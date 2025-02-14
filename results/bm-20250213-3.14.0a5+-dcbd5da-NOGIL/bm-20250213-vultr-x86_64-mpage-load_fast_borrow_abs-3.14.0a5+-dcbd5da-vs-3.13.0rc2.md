# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: dcbd5da
- commit date: 2025-02-13
- overall geometric mean: 1.028x slower
- HPT reliability: 98.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.73 sec: 1.04x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.4 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 335 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 304 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 248 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.30x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.1 ms: 1.06x faster                                                 |
| async_generators           | 375 ms                                                                 | 359 ms: 1.04x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.5 ms: 1.14x faster                                                 |
| pidigits       | 216 ms                                                                 | 209 ms: 1.04x faster                                                  |
| nbody          | 85.3 ms                                                                | 114 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.70 ms: 1.19x faster                                                 |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.04x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                                 |
| regex_compile  | 131 ms                                                                 | 141 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 85.5 ms: 1.10x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 224 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 92.8 ms: 1.09x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 326 us: 1.12x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 66.7 ms: 1.13x slower                                                 |
| json_loads           | 27.3 us                                                                | 31.1 us: 1.14x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.60 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 56.0 ms: 1.14x slower                                                 |
| django_template | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.0 ms: 1.20x slower                                                 |
| mako            | 11.2 ms                                                                | 15.0 ms: 1.34x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 335 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 304 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 248 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.30x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                  |
| deepcopy                   | 357 us                                                                 | 296 us: 1.21x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.70 ms: 1.19x faster                                                 |
| go                         | 141 ms                                                                 | 120 ms: 1.17x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 117 ms: 1.14x faster                                                  |
| float                      | 76.7 ms                                                                | 67.5 ms: 1.14x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 85.5 ms: 1.10x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.5 us: 1.10x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.1 ms: 1.06x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 65.4 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.98 us: 1.05x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 103 ms: 1.05x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.04x faster                                                  |
| async_generators           | 375 ms                                                                 | 359 ms: 1.04x faster                                                  |
| pidigits                   | 216 ms                                                                 | 209 ms: 1.04x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.42 sec: 1.01x faster                                                |
| scimark_fft                | 348 ms                                                                 | 352 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| regex_v8                   | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                                 |
| generators                 | 28.5 ms                                                                | 29.3 ms: 1.03x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                |
| logging_silent             | 98.2 ns                                                                | 101 ns: 1.03x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.73 sec: 1.04x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 755 ms: 1.05x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.20 ms: 1.05x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.55 sec: 1.07x slower                                                |
| regex_compile              | 131 ms                                                                 | 141 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 224 us: 1.07x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 80.3 ms: 1.08x slower                                                 |
| json                       | 4.98 ms                                                                | 5.39 ms: 1.08x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 92.8 ms: 1.09x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 115 ms: 1.09x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.24 ms: 1.10x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.43 ms: 1.11x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 58.3 ms: 1.11x slower                                                 |
| 2to3                       | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 326 us: 1.12x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.89 us: 1.12x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 66.7 ms: 1.13x slower                                                 |
| chaos                      | 56.3 ms                                                                | 63.4 ms: 1.13x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.71 ms: 1.13x slower                                                 |
| json_loads                 | 27.3 us                                                                | 31.1 us: 1.14x slower                                                 |
| richards                   | 44.4 ms                                                                | 50.6 ms: 1.14x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.88 us: 1.14x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 75.0 ms: 1.14x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 56.0 ms: 1.14x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.0 us: 1.14x slower                                                 |
| thrift                     | 772 us                                                                 | 882 us: 1.14x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.78 ms: 1.14x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| coverage                   | 82.5 ms                                                                | 95.6 ms: 1.16x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                                |
| richards_super             | 50.4 ms                                                                | 58.9 ms: 1.17x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 531 ms: 1.17x slower                                                  |
| raytrace                   | 250 ms                                                                 | 293 ms: 1.17x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.46 ms: 1.17x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 322 ms: 1.17x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.2 ms: 1.17x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 91.4 ms: 1.18x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.18x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 446 ms: 1.19x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 26.0 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 190 us: 1.22x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.23x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 83.8 ms: 1.23x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.60 ms: 1.29x slower                                                 |
| nbody                      | 85.3 ms                                                                | 114 ms: 1.33x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.0 ms: 1.34x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.25 ms: 3.52x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.1 ms: 8.56x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, pyflate
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250213-3.14.0a5+-dcbd5da-NOGIL/bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.028x slower

# HPT report

- Reliability score: 98.20% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x