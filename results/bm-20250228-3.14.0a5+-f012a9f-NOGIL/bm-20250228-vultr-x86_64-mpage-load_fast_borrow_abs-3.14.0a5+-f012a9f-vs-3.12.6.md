# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: f012a9f
- commit date: 2025-02-28
- overall geometric mean: 1.017x slower
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                                  |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                |
| html5lib       | 63.6 ms                                                | 71.6 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 537 ms: 2.07x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 572 ms: 1.89x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.9 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                  |
| nbody          | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.3 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 234 us: 1.06x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.25 sec: 1.07x slower                                                |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 344 us: 1.12x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.67 ms: 1.35x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                 |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 537 ms: 2.07x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.99x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 572 ms: 1.89x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| deepcopy                   | 352 us                                                 | 293 us: 1.20x faster                                                  |
| float                      | 80.8 ms                                                | 69.9 ms: 1.16x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 35.4 us: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| go                         | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.2 us: 1.03x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.60 sec: 1.03x faster                                                |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                  |
| scimark_sor                | 130 ms                                                 | 126 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.02 us: 1.02x faster                                                 |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| generators                 | 32.2 ms                                                | 32.7 ms: 1.01x slower                                                 |
| chaos                      | 62.8 ms                                                | 65.9 ms: 1.05x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.61 ms: 1.05x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 82.8 ms: 1.05x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                |
| pyflate                    | 448 ms                                                 | 474 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 234 us: 1.06x slower                                                  |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 793 ms: 1.07x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.25 sec: 1.07x slower                                                |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.64 sec: 1.08x slower                                                |
| thrift                     | 791 us                                                 | 859 us: 1.09x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.22 us: 1.09x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.83 ms: 1.09x slower                                                 |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.9 ms: 1.10x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.0 ms: 1.11x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.51 ms: 1.11x slower                                                 |
| logging_format             | 7.35 us                                                | 8.20 us: 1.12x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.4 ms: 1.12x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 344 us: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                 |
| html5lib                   | 63.6 ms                                                | 71.6 ms: 1.13x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.13x slower                                                |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 60.4 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 331 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| richards                   | 45.9 ms                                                | 52.8 ms: 1.15x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.6 ms: 1.15x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.10 ms: 1.15x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.15 ms: 1.17x slower                                                 |
| nqueens                    | 80.1 ms                                                | 94.0 ms: 1.17x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.18x slower                                                  |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.3 ms: 1.18x slower                                                 |
| richards_super             | 51.9 ms                                                | 61.2 ms: 1.18x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                 |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                 |
| fannkuch                   | 372 ms                                                 | 462 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| telco                      | 6.53 ms                                                | 8.39 ms: 1.29x slower                                                 |
| nbody                      | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.67 ms: 1.35x slower                                                 |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.36x slower                                                 |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.29 ms: 3.49x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.80x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (6): pylint, pycparser, asyncio_websockets, raytrace, scimark_fft, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-f012a9f-NOGIL/bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.017x slower

# HPT report

- Reliability score: 99.71% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x