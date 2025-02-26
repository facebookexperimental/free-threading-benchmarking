# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.020x slower
- HPT reliability: 99.88%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 71.7 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 544 ms: 2.04x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 575 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                  |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.00x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.9 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                                  |
| nbody          | 89.3 ms                                                | 118 ms: 1.32x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 345 us: 1.12x slower                                                  |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.65 ms: 1.35x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.7 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                 |
| django_template | 34.7 ms                                                | 42.3 ms: 1.22x slower                                                 |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 544 ms: 2.04x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.71 ms: 2.02x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 575 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                  |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                 |
| deepcopy                   | 352 us                                                 | 304 us: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.9 ms: 1.16x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 36.1 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                 |
| go                         | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.2 us: 1.03x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.61 sec: 1.03x faster                                                |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                                  |
| scimark_sor                | 130 ms                                                 | 129 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.00x faster                                                 |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                 |
| raytrace                   | 299 ms                                                 | 303 ms: 1.01x slower                                                  |
| generators                 | 32.2 ms                                                | 32.8 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.17 us: 1.03x slower                                                 |
| scimark_fft                | 342 ms                                                 | 356 ms: 1.04x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.62 ms: 1.05x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 83.0 ms: 1.05x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| chaos                      | 62.8 ms                                                | 66.2 ms: 1.05x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.57 sec: 1.06x slower                                                |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| pyflate                    | 448 ms                                                 | 478 ms: 1.07x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.19 us: 1.08x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 816 ms: 1.10x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.84 ms: 1.10x slower                                                 |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 84.8 ms: 1.11x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.0 ms: 1.11x slower                                                 |
| thrift                     | 791 us                                                 | 879 us: 1.11x slower                                                  |
| logging_format             | 7.35 us                                                | 8.17 us: 1.11x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 345 us: 1.12x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.8 us: 1.12x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.52 ms: 1.12x slower                                                 |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                                  |
| html5lib                   | 63.6 ms                                                | 71.7 ms: 1.13x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 60.2 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 330 ms: 1.13x slower                                                  |
| richards                   | 45.9 ms                                                | 52.3 ms: 1.14x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.6 ms: 1.15x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.7 ms: 1.15x slower                                                 |
| sympy_expand               | 468 ms                                                 | 541 ms: 1.16x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.18 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.16 ms: 1.17x slower                                                 |
| nqueens                    | 80.1 ms                                                | 94.2 ms: 1.18x slower                                                 |
| richards_super             | 51.9 ms                                                | 61.1 ms: 1.18x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.29 ms: 1.18x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                  |
| django_template            | 34.7 ms                                                | 42.3 ms: 1.22x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 465 ms: 1.25x slower                                                  |
| nbody                      | 89.3 ms                                                | 118 ms: 1.32x slower                                                  |
| telco                      | 6.53 ms                                                | 8.77 ms: 1.34x slower                                                 |
| coverage                   | 71.4 ms                                                | 96.2 ms: 1.35x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.65 ms: 1.35x slower                                                 |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.29 ms: 3.49x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.8 ms: 8.78x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (3): pylint, pycparser, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250225-3.14.0a5+-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 99.88% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x