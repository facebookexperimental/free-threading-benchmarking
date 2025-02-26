# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 596 ms: 1.51x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 598 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 484 ms: 1.38x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 305 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 472 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                  |
| async_generators           | 375 ms                                                                 | 316 ms: 1.19x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 21.7 ms: 1.08x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.31x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| float          | 76.7 ms                                                                | 70.2 ms: 1.09x faster                                                 |
| nbody          | 85.3 ms                                                                | 87.5 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 125 ms: 1.05x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 25.1 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.01 sec                                                               | 1.88 sec: 1.07x faster                                                |
| xml_etree_parse     | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| xml_etree_iterparse | 94.4 ms                                                                | 89.9 ms: 1.05x faster                                                 |
| xml_etree_generate  | 85.4 ms                                                                | 81.8 ms: 1.04x faster                                                 |
| xml_etree_process   | 59.2 ms                                                                | 57.3 ms: 1.03x faster                                                 |
| pickle_pure_python  | 292 us                                                                 | 302 us: 1.04x slower                                                  |
| json_dumps          | 10.6 ms                                                                | 11.1 ms: 1.05x slower                                                 |
| json_loads          | 27.3 us                                                                | 28.6 us: 1.05x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.52 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 46.4 ms: 1.06x faster                                                 |
| django_template | 34.2 ms                                                                | 32.8 ms: 1.04x faster                                                 |
| mako            | 11.2 ms                                                                | 11.4 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 596 ms: 1.51x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 598 ms: 1.47x faster                                                  |
| deepcopy                   | 357 us                                                                 | 246 us: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 484 ms: 1.38x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 305 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 472 ms: 1.34x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.7 us: 1.33x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                  |
| go                         | 141 ms                                                                 | 110 ms: 1.28x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 90.6 ms: 1.19x faster                                                 |
| async_generators           | 375 ms                                                                 | 316 ms: 1.19x faster                                                  |
| pylint                     | 317 ms                                                                 | 273 ms: 1.16x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 312 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                                 | 406 ms: 1.11x faster                                                  |
| pidigits                   | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.34 ms: 1.09x faster                                                 |
| float                      | 76.7 ms                                                                | 70.2 ms: 1.09x faster                                                 |
| thrift                     | 772 us                                                                 | 714 us: 1.08x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.21 ms: 1.08x faster                                                 |
| generators                 | 28.5 ms                                                                | 26.5 ms: 1.08x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 21.7 ms: 1.08x faster                                                 |
| richards                   | 44.4 ms                                                                | 41.3 ms: 1.07x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.88 sec: 1.07x faster                                                |
| richards_super             | 50.4 ms                                                                | 47.1 ms: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 673 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.18 sec: 1.07x faster                                                |
| genshi_text                | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.9 ms: 1.06x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.78 us: 1.06x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.52 us: 1.06x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.37 sec: 1.06x faster                                                |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 46.4 ms: 1.06x faster                                                 |
| regex_compile              | 131 ms                                                                 | 125 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.9 ms: 1.05x faster                                                 |
| chaos                      | 56.3 ms                                                                | 53.7 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 101 ms: 1.05x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 81.8 ms: 1.04x faster                                                 |
| django_template            | 34.2 ms                                                                | 32.8 ms: 1.04x faster                                                 |
| coverage                   | 82.5 ms                                                                | 79.2 ms: 1.04x faster                                                 |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 50.7 ms: 1.04x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                |
| hexiom                     | 5.95 ms                                                                | 5.74 ms: 1.04x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 57.3 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 151 us: 1.03x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 75.6 ms: 1.03x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 18.7 ms: 1.03x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 267 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 19.2 ms: 1.03x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 66.8 ms: 1.02x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 151 ms: 1.02x faster                                                  |
| mdp                        | 2.34 sec                                                               | 2.30 sec: 1.02x faster                                                |
| deltablue                  | 3.10 ms                                                                | 3.04 ms: 1.02x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 369 ms: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.02x faster                                                  |
| sympy_expand               | 454 ms                                                                 | 449 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.54 ms: 1.01x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 75.4 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.52 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.4 ms: 1.02x slower                                                 |
| nbody                      | 85.3 ms                                                                | 87.5 ms: 1.02x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 302 us: 1.04x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.1 ms: 1.05x slower                                                 |
| json_loads                 | 27.3 us                                                                | 28.6 us: 1.05x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 103 ns: 1.05x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 25.1 ms: 1.08x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.03 ms: 1.11x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.22 ms: 1.27x slower                                                 |
| python_startup             | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 88.0 ms: 8.00x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): sqlglot_parse, asyncio_websockets, unpickle_pure_python, json
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x