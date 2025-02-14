# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: dcbd5da
- commit date: 2025-02-13
- overall geometric mean: 1.005x faster
- HPT reliability: 92.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| docutils       | 2.64 sec                                               | 2.73 sec: 1.03x slower                                                |
| html5lib       | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 554 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 523 ms: 1.37x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                 |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.5 ms: 1.20x faster                                                 |
| pidigits       | 184 ms                                                 | 209 ms: 1.13x slower                                                  |
| nbody          | 89.3 ms                                                | 114 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                 |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.08x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 85.5 ms: 1.13x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.07 sec: 1.02x faster                                                |
| unpickle_pure_python | 221 us                                                 | 224 us: 1.01x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 326 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 92.8 ms: 1.09x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 66.7 ms: 1.13x slower                                                 |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.6 ms: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.0 ms: 1.12x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                 |
| django_template | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.0 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 554 ms: 2.00x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.99x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 523 ms: 1.37x faster                                                  |
| float                      | 80.8 ms                                                | 67.5 ms: 1.20x faster                                                 |
| deepcopy                   | 352 us                                                 | 296 us: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.5 us: 1.17x faster                                                 |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.14x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 85.5 ms: 1.13x faster                                                 |
| scimark_sor                | 130 ms                                                 | 117 ms: 1.11x faster                                                  |
| generators                 | 32.2 ms                                                | 29.3 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.07x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                                |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                  |
| spectral_norm              | 110 ms                                                 | 103 ms: 1.07x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.0 us: 1.05x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.98 us: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.07 sec: 1.02x faster                                                |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.43 ms: 1.01x faster                                                 |
| chaos                      | 62.8 ms                                                | 63.4 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 224 us: 1.01x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 755 ms: 1.02x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 80.3 ms: 1.02x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.55 sec: 1.02x slower                                                |
| html5lib                   | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                 |
| scimark_fft                | 342 ms                                                 | 352 ms: 1.03x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.73 sec: 1.03x slower                                                |
| logging_simple             | 6.63 us                                                | 6.89 us: 1.04x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 326 us: 1.06x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.78 ms: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                 |
| logging_format             | 7.35 us                                                | 7.88 us: 1.07x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.08x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.46 ms: 1.08x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 115 ms: 1.08x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.71 ms: 1.09x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 92.8 ms: 1.09x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 83.8 ms: 1.09x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 58.3 ms: 1.10x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 75.0 ms: 1.10x slower                                                 |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| richards                   | 45.9 ms                                                | 50.6 ms: 1.10x slower                                                 |
| sympy_str                  | 292 ms                                                 | 322 ms: 1.10x slower                                                  |
| thrift                     | 791 us                                                 | 882 us: 1.11x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 56.0 ms: 1.12x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.12x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 23.2 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 66.7 ms: 1.13x slower                                                 |
| pidigits                   | 184 ms                                                 | 209 ms: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 531 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 58.9 ms: 1.14x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                 |
| nqueens                    | 80.1 ms                                                | 91.4 ms: 1.14x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| django_template            | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.24 ms: 1.19x slower                                                 |
| fannkuch                   | 372 ms                                                 | 446 ms: 1.20x slower                                                  |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.6 ms: 1.22x slower                                                 |
| telco                      | 6.53 ms                                                | 8.20 ms: 1.26x slower                                                 |
| nbody                      | 89.3 ms                                                | 114 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                                 |
| coverage                   | 71.4 ms                                                | 95.6 ms: 1.34x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                 |
| mako                       | 11.0 ms                                                | 15.0 ms: 1.36x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.25 ms: 3.45x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.1 ms: 8.72x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, pyflate
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250213-3.14.0a5+-dcbd5da-NOGIL/bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 92.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x