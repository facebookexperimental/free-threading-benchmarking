# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 6c2f07d
- commit date: 2025-03-17
- overall geometric mean: 1.020x slower
- HPT reliability: 99.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 69.6 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 540 ms: 2.06x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 570 ms: 1.90x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                  |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.8 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                  |
| nbody          | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_compile  | 142 ms                                                 | 153 ms: 1.07x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.26 sec: 1.07x slower                                                |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.09x slower                                                  |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.9 ms: 1.17x slower                                                 |
| django_template | 34.7 ms                                                | 41.7 ms: 1.20x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.6 ms: 1.21x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 540 ms: 2.06x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.72 ms: 2.01x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 570 ms: 1.90x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                  |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| deepcopy                   | 352 us                                                 | 302 us: 1.17x faster                                                  |
| float                      | 80.8 ms                                                | 71.8 ms: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 36.3 us: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 73.7 ms: 1.07x faster                                                 |
| go                         | 139 ms                                                 | 132 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                  |
| scimark_sor                | 130 ms                                                 | 127 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.66 sec: 1.02x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.11 us: 1.01x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| scimark_fft                | 342 ms                                                 | 356 ms: 1.04x slower                                                  |
| chaos                      | 62.8 ms                                                | 65.5 ms: 1.04x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.59 ms: 1.04x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 796 ms: 1.07x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.26 sec: 1.07x slower                                                |
| regex_compile              | 142 ms                                                 | 153 ms: 1.07x slower                                                  |
| pyflate                    | 448 ms                                                 | 483 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.64 sec: 1.08x slower                                                |
| logging_simple             | 6.63 us                                                | 7.18 us: 1.08x slower                                                 |
| thrift                     | 791 us                                                 | 858 us: 1.08x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.83 ms: 1.09x slower                                                 |
| html5lib                   | 63.6 ms                                                | 69.6 ms: 1.10x slower                                                 |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.9 ms: 1.10x slower                                                 |
| logging_format             | 7.35 us                                                | 8.08 us: 1.10x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 118 ms: 1.11x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.51 ms: 1.11x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.2 ms: 1.11x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                                |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.11x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 76.6 ms: 1.12x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 60.2 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                                  |
| richards                   | 45.9 ms                                                | 53.1 ms: 1.16x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.8 ms: 1.16x slower                                                 |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.9 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                 |
| richards_super             | 51.9 ms                                                | 61.7 ms: 1.19x slower                                                 |
| nqueens                    | 80.1 ms                                                | 95.4 ms: 1.19x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.31 ms: 1.20x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.28 ms: 1.20x slower                                                 |
| django_template            | 34.7 ms                                                | 41.7 ms: 1.20x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.6 ms: 1.21x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                  |
| fannkuch                   | 372 ms                                                 | 470 ms: 1.26x slower                                                  |
| telco                      | 6.53 ms                                                | 8.44 ms: 1.29x slower                                                 |
| nbody                      | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| coverage                   | 71.4 ms                                                | 96.3 ms: 1.35x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 95.3 ms: 8.82x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (5): pylint, comprehensions, generators, asyncio_websockets, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250317-3.14.0a6+-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 99.49% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x