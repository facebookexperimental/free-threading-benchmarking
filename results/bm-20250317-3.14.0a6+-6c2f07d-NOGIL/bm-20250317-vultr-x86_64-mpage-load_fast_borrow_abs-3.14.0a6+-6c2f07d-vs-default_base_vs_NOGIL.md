# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 6c2f07d
- commit date: 2025-03-17
- overall geometric mean: 1.079x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 289 ms: 1.12x slower                                                  |
| docutils       | 2.61 sec                                                               | 2.78 sec: 1.06x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.08 sec: 1.08x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 540 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 260 ms                                                                 | 234 ms: 1.11x faster                                                  |
| async_tree_io              | 630 ms                                                                 | 570 ms: 1.10x faster                                                  |
| async_tree_memoization_tg  | 315 ms                                                                 | 301 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 487 ms: 1.02x faster                                                  |
| async_tree_none            | 274 ms                                                                 | 269 ms: 1.02x faster                                                  |
| async_tree_memoization     | 327 ms                                                                 | 331 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 518 ms: 1.01x slower                                                  |
| async_generators           | 340 ms                                                                 | 369 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 74.5 ms                                                                | 71.8 ms: 1.04x faster                                                 |
| pidigits       | 206 ms                                                                 | 200 ms: 1.03x faster                                                  |
| nbody          | 99.0 ms                                                                | 119 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.3 ms                                                                | 23.3 ms: 1.05x faster                                                 |
| regex_dna      | 177 ms                                                                 | 174 ms: 1.02x faster                                                  |
| regex_effbot   | 2.64 ms                                                                | 2.83 ms: 1.07x slower                                                 |
| regex_compile  | 128 ms                                                                 | 153 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.6 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.02x faster                                                  |
| json_loads           | 28.4 us                                                                | 29.3 us: 1.03x slower                                                 |
| pickle_pure_python   | 322 us                                                                 | 343 us: 1.06x slower                                                  |
| unpickle_pure_python | 223 us                                                                 | 239 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.7 ms                                                                | 96.6 ms: 1.13x slower                                                 |
| json_dumps           | 11.2 ms                                                                | 12.7 ms: 1.14x slower                                                 |
| tomli_loads          | 1.98 sec                                                               | 2.26 sec: 1.14x slower                                                |
| xml_etree_process    | 59.7 ms                                                                | 69.4 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.0 ms                                                                | 15.7 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.62 ms                                                                | 11.1 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.5 ms                                                                | 41.7 ms: 1.14x slower                                                 |
| genshi_xml      | 51.0 ms                                                                | 58.9 ms: 1.15x slower                                                 |
| genshi_text     | 22.5 ms                                                                | 27.6 ms: 1.23x slower                                                 |
| mako            | 12.2 ms                                                                | 15.6 ms: 1.28x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.16 ms                                                                | 1.72 ms: 2.42x faster                                                 |
| create_gc_cycles           | 1.82 ms                                                                | 1.31 ms: 1.39x faster                                                 |
| async_tree_io_tg           | 628 ms                                                                 | 540 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 260 ms                                                                 | 234 ms: 1.11x faster                                                  |
| async_tree_io              | 630 ms                                                                 | 570 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.19 us                                                                | 2.05 us: 1.07x faster                                                 |
| xml_etree_iterparse        | 93.6 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| regex_v8                   | 24.3 ms                                                                | 23.3 ms: 1.05x faster                                                 |
| async_tree_memoization_tg  | 315 ms                                                                 | 301 ms: 1.05x faster                                                  |
| float                      | 74.5 ms                                                                | 71.8 ms: 1.04x faster                                                 |
| pidigits                   | 206 ms                                                                 | 200 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 487 ms: 1.02x faster                                                  |
| async_tree_none            | 274 ms                                                                 | 269 ms: 1.02x faster                                                  |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.02x faster                                                  |
| regex_dna                  | 177 ms                                                                 | 174 ms: 1.02x faster                                                  |
| pycparser                  | 1.15 sec                                                               | 1.16 sec: 1.00x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| async_tree_memoization     | 327 ms                                                                 | 331 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 518 ms: 1.01x slower                                                  |
| logging_silent             | 103 ns                                                                 | 105 ns: 1.02x slower                                                  |
| json_loads                 | 28.4 us                                                                | 29.3 us: 1.03x slower                                                 |
| python_startup             | 15.0 ms                                                                | 15.7 ms: 1.05x slower                                                 |
| docutils                   | 2.61 sec                                                               | 2.78 sec: 1.06x slower                                                |
| pickle_pure_python         | 322 us                                                                 | 343 us: 1.06x slower                                                  |
| bpe_tokeniser              | 4.37 sec                                                               | 4.66 sec: 1.07x slower                                                |
| regex_effbot               | 2.64 ms                                                                | 2.83 ms: 1.07x slower                                                 |
| unpickle_pure_python       | 223 us                                                                 | 239 us: 1.07x slower                                                  |
| bench_mp_pool              | 88.4 ms                                                                | 95.3 ms: 1.08x slower                                                 |
| sphinx                     | 1.00 sec                                                               | 1.08 sec: 1.08x slower                                                |
| scimark_fft                | 329 ms                                                                 | 356 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 736 ms                                                                 | 796 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                                               | 1.64 sec: 1.08x slower                                                |
| dulwich_log                | 68.0 ms                                                                | 73.7 ms: 1.08x slower                                                 |
| generators                 | 29.7 ms                                                                | 32.2 ms: 1.09x slower                                                 |
| async_generators           | 340 ms                                                                 | 369 ms: 1.09x slower                                                  |
| scimark_sparse_mat_mult    | 4.84 ms                                                                | 5.28 ms: 1.09x slower                                                 |
| k_core                     | 2.07 sec                                                               | 2.27 sec: 1.09x slower                                                |
| subparsers                 | 22.9 ms                                                                | 25.2 ms: 1.10x slower                                                 |
| many_optionals             | 1.04 ms                                                                | 1.15 ms: 1.10x slower                                                 |
| scimark_sor                | 115 ms                                                                 | 127 ms: 1.11x slower                                                  |
| pylint                     | 284 ms                                                                 | 315 ms: 1.11x slower                                                  |
| raytrace                   | 271 ms                                                                 | 301 ms: 1.11x slower                                                  |
| chaos                      | 59.0 ms                                                                | 65.5 ms: 1.11x slower                                                 |
| telco                      | 7.56 ms                                                                | 8.44 ms: 1.12x slower                                                 |
| 2to3                       | 258 ms                                                                 | 289 ms: 1.12x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 118 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.7 ms                                                                | 96.6 ms: 1.13x slower                                                 |
| pyflate                    | 427 ms                                                                 | 483 ms: 1.13x slower                                                  |
| go                         | 116 ms                                                                 | 132 ms: 1.13x slower                                                  |
| sqlglot_optimize           | 53.2 ms                                                                | 60.2 ms: 1.13x slower                                                 |
| deltablue                  | 3.17 ms                                                                | 3.59 ms: 1.14x slower                                                 |
| deepcopy                   | 266 us                                                                 | 302 us: 1.14x slower                                                  |
| json_dumps                 | 11.2 ms                                                                | 12.7 ms: 1.14x slower                                                 |
| deepcopy_reduce            | 2.74 us                                                                | 3.11 us: 1.14x slower                                                 |
| nqueens                    | 83.8 ms                                                                | 95.4 ms: 1.14x slower                                                 |
| tomli_loads                | 1.98 sec                                                               | 2.26 sec: 1.14x slower                                                |
| scimark_monte_carlo        | 67.1 ms                                                                | 76.6 ms: 1.14x slower                                                 |
| django_template            | 36.5 ms                                                                | 41.7 ms: 1.14x slower                                                 |
| mdp                        | 2.35 sec                                                               | 2.69 sec: 1.14x slower                                                |
| sqlglot_transpile          | 1.60 ms                                                                | 1.83 ms: 1.14x slower                                                 |
| thrift                     | 748 us                                                                 | 858 us: 1.15x slower                                                  |
| spectral_norm              | 93.1 ms                                                                | 107 ms: 1.15x slower                                                  |
| sympy_expand               | 475 ms                                                                 | 548 ms: 1.15x slower                                                  |
| genshi_xml                 | 51.0 ms                                                                | 58.9 ms: 1.15x slower                                                 |
| comprehensions             | 17.0 us                                                                | 19.8 us: 1.16x slower                                                 |
| xml_etree_process          | 59.7 ms                                                                | 69.4 ms: 1.16x slower                                                 |
| fannkuch                   | 403 ms                                                                 | 470 ms: 1.17x slower                                                  |
| sqlglot_parse              | 1.29 ms                                                                | 1.51 ms: 1.17x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.18 us: 1.17x slower                                                 |
| deepcopy_memo              | 30.8 us                                                                | 36.3 us: 1.18x slower                                                 |
| sympy_sum                  | 157 ms                                                                 | 185 ms: 1.18x slower                                                  |
| sympy_integrate            | 20.1 ms                                                                | 23.8 ms: 1.18x slower                                                 |
| logging_format             | 6.83 us                                                                | 8.08 us: 1.18x slower                                                 |
| sympy_str                  | 280 ms                                                                 | 333 ms: 1.19x slower                                                  |
| coverage                   | 81.1 ms                                                                | 96.3 ms: 1.19x slower                                                 |
| crypto_pyaes               | 71.8 ms                                                                | 85.2 ms: 1.19x slower                                                 |
| scimark_lu                 | 117 ms                                                                 | 139 ms: 1.19x slower                                                  |
| regex_compile              | 128 ms                                                                 | 153 ms: 1.19x slower                                                  |
| nbody                      | 99.0 ms                                                                | 119 ms: 1.20x slower                                                  |
| sqlalchemy_declarative     | 131 ms                                                                 | 158 ms: 1.21x slower                                                  |
| hexiom                     | 6.10 ms                                                                | 7.39 ms: 1.21x slower                                                 |
| shortest_path              | 443 ms                                                                 | 537 ms: 1.21x slower                                                  |
| connected_components       | 403 ms                                                                 | 489 ms: 1.22x slower                                                  |
| meteor_contest             | 105 ms                                                                 | 128 ms: 1.23x slower                                                  |
| genshi_text                | 22.5 ms                                                                | 27.6 ms: 1.23x slower                                                 |
| sqlalchemy_imperative      | 19.5 ms                                                                | 23.9 ms: 1.23x slower                                                 |
| richards                   | 43.2 ms                                                                | 53.1 ms: 1.23x slower                                                 |
| typing_runtime_protocols   | 157 us                                                                 | 196 us: 1.25x slower                                                  |
| richards_super             | 49.2 ms                                                                | 61.7 ms: 1.25x slower                                                 |
| mako                       | 12.2 ms                                                                | 15.6 ms: 1.28x slower                                                 |
| python_startup_no_site     | 8.62 ms                                                                | 11.1 ms: 1.28x slower                                                 |
| bench_thread_pool          | 1.05 ms                                                                | 3.13 ms: 2.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (3): coroutines, json, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250317-3.14.0a6+-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d.json: html5lib

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x