# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: f012a9f
- commit date: 2025-02-28
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 248 ms: 1.05x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 601 ms: 1.50x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 314 ms: 1.46x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 263 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 257 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 318 ms: 1.18x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.1 ms: 1.09x faster                                                 |
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                                  |
| nbody          | 85.3 ms                                                                | 87.3 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.70 ms: 1.19x faster                                                 |
| regex_dna      | 189 ms                                                                 | 174 ms: 1.08x faster                                                  |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| xml_etree_parse     | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| xml_etree_iterparse | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                 |
| xml_etree_generate  | 85.4 ms                                                                | 82.3 ms: 1.04x faster                                                 |
| xml_etree_process   | 59.2 ms                                                                | 57.1 ms: 1.04x faster                                                 |
| json_dumps          | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                                 |
| pickle_pure_python  | 292 us                                                                 | 302 us: 1.04x slower                                                  |
| json_loads          | 27.3 us                                                                | 28.8 us: 1.05x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.50 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 47.5 ms: 1.03x faster                                                 |
| django_template | 34.2 ms                                                                | 33.3 ms: 1.03x faster                                                 |
| mako            | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 601 ms: 1.50x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 314 ms: 1.46x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                  |
| deepcopy                   | 357 us                                                                 | 245 us: 1.46x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 263 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 498 ms: 1.34x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.8 us: 1.32x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 257 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                  |
| go                         | 141 ms                                                                 | 111 ms: 1.27x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.53 us: 1.24x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.20x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.70 ms: 1.19x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 91.2 ms: 1.18x faster                                                 |
| async_generators           | 375 ms                                                                 | 318 ms: 1.18x faster                                                  |
| pylint                     | 317 ms                                                                 | 274 ms: 1.16x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.11 ms: 1.16x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 310 ms: 1.12x faster                                                  |
| pyflate                    | 449 ms                                                                 | 404 ms: 1.11x faster                                                  |
| float                      | 76.7 ms                                                                | 70.1 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.12 sec: 1.08x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| regex_dna                  | 189 ms                                                                 | 174 ms: 1.08x faster                                                  |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.36 sec: 1.07x faster                                                |
| pprint_safe_repr           | 719 ms                                                                 | 672 ms: 1.07x faster                                                  |
| thrift                     | 772 us                                                                 | 722 us: 1.07x faster                                                  |
| richards                   | 44.4 ms                                                                | 41.7 ms: 1.06x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.62 ms: 1.06x faster                                                 |
| richards_super             | 50.4 ms                                                                | 47.6 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 106 ms: 1.06x faster                                                  |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.36 ms: 1.06x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.85 us: 1.05x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.2 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.9 ms: 1.05x faster                                                 |
| 2to3                       | 259 ms                                                                 | 248 ms: 1.05x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 74.4 ms: 1.05x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| chaos                      | 56.3 ms                                                                | 54.1 ms: 1.04x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 82.3 ms: 1.04x faster                                                 |
| coverage                   | 82.5 ms                                                                | 79.4 ms: 1.04x faster                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 102 ms: 1.04x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 57.1 ms: 1.04x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 50.8 ms: 1.04x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 47.5 ms: 1.03x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.71 us: 1.03x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 98.7 ms: 1.03x faster                                                 |
| django_template            | 34.2 ms                                                                | 33.3 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 152 us: 1.03x faster                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 66.5 ms: 1.03x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.52 ms: 1.02x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 268 ms: 1.02x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 151 ms: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| sqlglot_parse              | 1.25 ms                                                                | 1.22 ms: 1.02x faster                                                 |
| mdp                        | 2.34 sec                                                               | 2.30 sec: 1.02x faster                                                |
| sympy_integrate            | 19.7 ms                                                                | 19.4 ms: 1.02x faster                                                 |
| deltablue                  | 3.10 ms                                                                | 3.06 ms: 1.01x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 373 ms: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.2 ms: 1.01x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 451 ms: 1.01x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 75.1 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.50 ms: 1.01x slower                                                 |
| regex_v8                   | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 255 ms: 1.02x slower                                                  |
| nbody                      | 85.3 ms                                                                | 87.3 ms: 1.02x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 302 us: 1.04x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 103 ns: 1.05x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.8 us: 1.05x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.03 ms: 1.12x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.44 ms: 1.34x slower                                                 |
| python_startup             | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.83 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 87.8 ms: 7.98x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, unpickle_pure_python, json
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250228-3.14.0a5+-f012a9f/bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x