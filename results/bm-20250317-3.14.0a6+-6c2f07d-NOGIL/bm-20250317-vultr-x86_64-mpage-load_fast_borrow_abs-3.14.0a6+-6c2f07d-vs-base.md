# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 6c2f07d
- commit date: 2025-03-17
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                 | 289 ms: 1.03x faster                                                  |
| docutils       | 2.79 sec                                                               | 2.78 sec: 1.01x faster                                                |
| html5lib       | 72.2 ms                                                                | 69.6 ms: 1.04x faster                                                 |
| sphinx         | 1.10 sec                                                               | 1.08 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 23.9 ms                                                                | 23.1 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 556 ms                                                                 | 540 ms: 1.03x faster                                                  |
| async_generators           | 379 ms                                                                 | 369 ms: 1.03x faster                                                  |
| async_tree_none            | 276 ms                                                                 | 269 ms: 1.03x faster                                                  |
| async_tree_memoization     | 339 ms                                                                 | 331 ms: 1.02x faster                                                  |
| async_tree_io              | 581 ms                                                                 | 570 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 301 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 237 ms                                                                 | 234 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 490 ms                                                                 | 487 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 119 ms: 1.14x faster                                                  |
| float          | 76.8 ms                                                                | 71.8 ms: 1.07x faster                                                 |
| pidigits       | 201 ms                                                                 | 200 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 174 ms: 1.07x faster                                                  |
| regex_v8       | 24.2 ms                                                                | 23.3 ms: 1.04x faster                                                 |
| regex_compile  | 158 ms                                                                 | 153 ms: 1.03x faster                                                  |
| regex_effbot   | 2.78 ms                                                                | 2.83 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 252 us                                                                 | 239 us: 1.05x faster                                                  |
| pickle_pure_python   | 357 us                                                                 | 343 us: 1.04x faster                                                  |
| tomli_loads          | 2.34 sec                                                               | 2.26 sec: 1.04x faster                                                |
| json_dumps           | 12.9 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 88.5 ms                                                                | 87.9 ms: 1.01x faster                                                 |
| xml_etree_process    | 69.6 ms                                                                | 69.4 ms: 1.00x faster                                                 |
| json_loads           | 29.1 us                                                                | 29.3 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 28.8 ms                                                                | 27.6 ms: 1.04x faster                                                 |
| genshi_xml      | 60.5 ms                                                                | 58.9 ms: 1.03x faster                                                 |
| mako            | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                                 |
| django_template | 42.3 ms                                                                | 41.7 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 136 ms                                                                 | 119 ms: 1.14x faster                                                  |
| scimark_fft                | 389 ms                                                                 | 356 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 5.77 ms                                                                | 5.28 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 83.1 ms                                                                | 76.6 ms: 1.08x faster                                                 |
| regex_dna                  | 187 ms                                                                 | 174 ms: 1.07x faster                                                  |
| go                         | 141 ms                                                                 | 132 ms: 1.07x faster                                                  |
| float                      | 76.8 ms                                                                | 71.8 ms: 1.07x faster                                                 |
| raytrace                   | 322 ms                                                                 | 301 ms: 1.07x faster                                                  |
| pyflate                    | 515 ms                                                                 | 483 ms: 1.07x faster                                                  |
| scimark_sor                | 136 ms                                                                 | 127 ms: 1.06x faster                                                  |
| deepcopy_memo              | 38.6 us                                                                | 36.3 us: 1.06x faster                                                 |
| sqlglot_parse              | 1.60 ms                                                                | 1.51 ms: 1.06x faster                                                 |
| chaos                      | 69.5 ms                                                                | 65.5 ms: 1.06x faster                                                 |
| deltablue                  | 3.81 ms                                                                | 3.59 ms: 1.06x faster                                                 |
| pprint_safe_repr           | 841 ms                                                                 | 796 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.73 sec                                                               | 1.64 sec: 1.05x faster                                                |
| unpickle_pure_python       | 252 us                                                                 | 239 us: 1.05x faster                                                  |
| fannkuch                   | 495 ms                                                                 | 470 ms: 1.05x faster                                                  |
| logging_silent             | 111 ns                                                                 | 105 ns: 1.05x faster                                                  |
| sqlglot_transpile          | 1.92 ms                                                                | 1.83 ms: 1.05x faster                                                 |
| comprehensions             | 20.7 us                                                                | 19.8 us: 1.05x faster                                                 |
| meteor_contest             | 134 ms                                                                 | 128 ms: 1.04x faster                                                  |
| genshi_text                | 28.8 ms                                                                | 27.6 ms: 1.04x faster                                                 |
| pickle_pure_python         | 357 us                                                                 | 343 us: 1.04x faster                                                  |
| regex_v8                   | 24.2 ms                                                                | 23.3 ms: 1.04x faster                                                 |
| tomli_loads                | 2.34 sec                                                               | 2.26 sec: 1.04x faster                                                |
| crypto_pyaes               | 88.5 ms                                                                | 85.2 ms: 1.04x faster                                                 |
| bpe_tokeniser              | 4.84 sec                                                               | 4.66 sec: 1.04x faster                                                |
| html5lib                   | 72.2 ms                                                                | 69.6 ms: 1.04x faster                                                 |
| spectral_norm              | 111 ms                                                                 | 107 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                                | 23.1 ms: 1.03x faster                                                 |
| regex_compile              | 158 ms                                                                 | 153 ms: 1.03x faster                                                  |
| 2to3                       | 298 ms                                                                 | 289 ms: 1.03x faster                                                  |
| nqueens                    | 98.4 ms                                                                | 95.4 ms: 1.03x faster                                                 |
| richards                   | 54.7 ms                                                                | 53.1 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 556 ms                                                                 | 540 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                                               | 1.16 sec: 1.03x faster                                                |
| deepcopy                   | 310 us                                                                 | 302 us: 1.03x faster                                                  |
| genshi_xml                 | 60.5 ms                                                                | 58.9 ms: 1.03x faster                                                 |
| async_generators           | 379 ms                                                                 | 369 ms: 1.03x faster                                                  |
| hexiom                     | 7.58 ms                                                                | 7.39 ms: 1.03x faster                                                 |
| connected_components       | 502 ms                                                                 | 489 ms: 1.03x faster                                                  |
| async_tree_none            | 276 ms                                                                 | 269 ms: 1.03x faster                                                  |
| richards_super             | 63.2 ms                                                                | 61.7 ms: 1.03x faster                                                 |
| telco                      | 8.66 ms                                                                | 8.44 ms: 1.03x faster                                                 |
| thrift                     | 879 us                                                                 | 858 us: 1.03x faster                                                  |
| create_gc_cycles           | 1.34 ms                                                                | 1.31 ms: 1.02x faster                                                 |
| logging_format             | 8.28 us                                                                | 8.08 us: 1.02x faster                                                 |
| async_tree_memoization     | 339 ms                                                                 | 331 ms: 1.02x faster                                                  |
| shortest_path              | 548 ms                                                                 | 537 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 61.6 ms                                                                | 60.2 ms: 1.02x faster                                                 |
| scimark_lu                 | 142 ms                                                                 | 139 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 121 ms                                                                 | 118 ms: 1.02x faster                                                  |
| gc_traversal               | 1.75 ms                                                                | 1.72 ms: 1.02x faster                                                 |
| coverage                   | 98.2 ms                                                                | 96.3 ms: 1.02x faster                                                 |
| deepcopy_reduce            | 3.17 us                                                                | 3.11 us: 1.02x faster                                                 |
| async_tree_io              | 581 ms                                                                 | 570 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 301 ms: 1.02x faster                                                  |
| mako                       | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                                 |
| json_dumps                 | 12.9 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| k_core                     | 2.30 sec                                                               | 2.27 sec: 1.01x faster                                                |
| django_template            | 42.3 ms                                                                | 41.7 ms: 1.01x faster                                                 |
| sympy_integrate            | 24.1 ms                                                                | 23.8 ms: 1.01x faster                                                 |
| async_tree_none_tg         | 237 ms                                                                 | 234 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 198 us                                                                 | 196 us: 1.01x faster                                                  |
| many_optionals             | 1.17 ms                                                                | 1.15 ms: 1.01x faster                                                 |
| pathlib                    | 19.7 ms                                                                | 19.5 ms: 1.01x faster                                                 |
| sympy_str                  | 336 ms                                                                 | 333 ms: 1.01x faster                                                  |
| sphinx                     | 1.10 sec                                                               | 1.08 sec: 1.01x faster                                                |
| async_tree_cpu_io_mixed    | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 88.5 ms                                                                | 87.9 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 490 ms                                                                 | 487 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.15 ms                                                                | 3.13 ms: 1.01x faster                                                 |
| sympy_sum                  | 186 ms                                                                 | 185 ms: 1.01x faster                                                  |
| docutils                   | 2.79 sec                                                               | 2.78 sec: 1.01x faster                                                |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| pidigits                   | 201 ms                                                                 | 200 ms: 1.01x faster                                                  |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                 |
| xml_etree_process          | 69.6 ms                                                                | 69.4 ms: 1.00x faster                                                 |
| dulwich_log                | 73.3 ms                                                                | 73.7 ms: 1.01x slower                                                 |
| json_loads                 | 29.1 us                                                                | 29.3 us: 1.01x slower                                                 |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.01x slower                                                  |
| mdp                        | 2.67 sec                                                               | 2.69 sec: 1.01x slower                                                |
| sqlite_synth               | 2.03 us                                                                | 2.05 us: 1.01x slower                                                 |
| regex_effbot               | 2.78 ms                                                                | 2.83 ms: 1.02x slower                                                 |
| sqlalchemy_imperative      | 23.5 ms                                                                | 23.9 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (10): json, logging_simple, sympy_expand, generators, xml_etree_parse, xml_etree_generate, asyncio_websockets, pylint, bench_mp_pool, subparsers

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x