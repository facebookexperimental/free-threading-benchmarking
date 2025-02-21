# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 1998b35
- commit date: 2025-02-21
- overall geometric mean: 1.002x faster
- HPT reliability: 96.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 287 ms: 1.09x slower                                                  |
| docutils       | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                |
| html5lib       | 63.6 ms                                                | 67.1 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 293 ms: 1.91x faster                                                  |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 527 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 559 ms: 1.28x faster                                                  |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.9 ms: 1.17x faster                                                 |
| nbody          | 89.3 ms                                                | 114 ms: 1.27x slower                                                  |
| pidigits       | 184 ms                                                 | 240 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 85.6 ms: 1.13x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 330 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 92.4 ms: 1.08x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 66.4 ms: 1.13x slower                                                 |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.65 ms: 1.35x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.7 ms: 1.11x slower                                                 |
| genshi_text     | 22.8 ms                                                | 25.3 ms: 1.11x slower                                                 |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 15.1 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.97x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 293 ms: 1.91x faster                                                  |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 527 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 559 ms: 1.28x faster                                                  |
| deepcopy                   | 352 us                                                 | 292 us: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 68.9 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.9 us: 1.16x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 85.6 ms: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| generators                 | 32.2 ms                                                | 29.6 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                  |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| comprehensions             | 19.8 us                                                | 18.6 us: 1.06x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.48 sec: 1.06x faster                                                |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.05x faster                                                  |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                  |
| raytrace                   | 299 ms                                                 | 290 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| pyflate                    | 448 ms                                                 | 452 ms: 1.01x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.5 ms: 1.01x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.48 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 761 ms: 1.02x slower                                                  |
| scimark_fft                | 342 ms                                                 | 351 ms: 1.03x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.57 sec: 1.03x slower                                                |
| dulwich_log                | 78.9 ms                                                | 81.6 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.96 us: 1.05x slower                                                 |
| json                       | 5.02 ms                                                | 5.28 ms: 1.05x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.1 ms: 1.06x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.78 ms: 1.06x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 330 us: 1.07x slower                                                  |
| richards                   | 45.9 ms                                                | 49.5 ms: 1.08x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 115 ms: 1.08x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 154 ms: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| logging_format             | 7.35 us                                                | 7.96 us: 1.08x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 92.4 ms: 1.08x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.47 ms: 1.08x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 74.3 ms: 1.09x slower                                                 |
| 2to3                       | 264 ms                                                 | 287 ms: 1.09x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 83.4 ms: 1.09x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.10x slower                                                  |
| sympy_str                  | 292 ms                                                 | 321 ms: 1.10x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 58.7 ms: 1.10x slower                                                 |
| thrift                     | 791 us                                                 | 873 us: 1.10x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.82 ms: 1.11x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 55.7 ms: 1.11x slower                                                 |
| genshi_text                | 22.8 ms                                                | 25.3 ms: 1.11x slower                                                 |
| richards_super             | 51.9 ms                                                | 57.7 ms: 1.11x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.70 sec: 1.12x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 66.4 ms: 1.13x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.1 ms: 1.13x slower                                                 |
| sympy_expand               | 468 ms                                                 | 529 ms: 1.13x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                 |
| nqueens                    | 80.1 ms                                                | 91.0 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.11 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                  |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| nbody                      | 89.3 ms                                                | 114 ms: 1.27x slower                                                  |
| pidigits                   | 184 ms                                                 | 240 ms: 1.30x slower                                                  |
| telco                      | 6.53 ms                                                | 8.59 ms: 1.32x slower                                                 |
| coverage                   | 71.4 ms                                                | 95.7 ms: 1.34x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.65 ms: 1.35x slower                                                 |
| mako                       | 11.0 ms                                                | 15.1 ms: 1.38x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.26 ms: 3.46x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 95.1 ms: 8.81x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, deepcopy_reduce
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250221-3.14.0a5+-1998b35-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 96.18% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x