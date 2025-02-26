# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: b10c3be
- commit date: 2025-02-26
- overall geometric mean: 1.101x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                  |
| async_generators           | 384 ms                                                 | 319 ms: 1.21x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.11x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.8 ms: 1.17x faster                                                 |
| nbody          | 89.3 ms                                                | 86.4 ms: 1.03x faster                                                 |
| pidigits       | 184 ms                                                 | 189 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 81.6 ms: 1.04x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 56.8 ms: 1.04x faster                                                 |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 46.5 ms: 1.08x faster                                                 |
| django_template | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                 |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                  |
| deepcopy                   | 352 us                                                 | 248 us: 1.42x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.0 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 111 ms: 1.26x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.25x faster                                                 |
| spectral_norm              | 110 ms                                                 | 89.5 ms: 1.23x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.53 us: 1.22x faster                                                 |
| async_generators           | 384 ms                                                 | 319 ms: 1.21x faster                                                  |
| generators                 | 32.2 ms                                                | 26.8 ms: 1.20x faster                                                 |
| float                      | 80.8 ms                                                | 68.8 ms: 1.17x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 65.3 ms: 1.17x faster                                                 |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                  |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                                  |
| pylint                     | 319 ms                                                 | 273 ms: 1.17x faster                                                  |
| chaos                      | 62.8 ms                                                | 53.8 ms: 1.17x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.14 sec: 1.14x faster                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.04 ms: 1.13x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.89 us: 1.13x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.22 ms: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.59 us: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| scimark_fft                | 342 ms                                                 | 307 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 61.7 ms: 1.11x faster                                                 |
| richards                   | 45.9 ms                                                | 41.6 ms: 1.11x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                 |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.11x faster                                                 |
| thrift                     | 791 us                                                 | 718 us: 1.10x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.38 sec: 1.10x faster                                                |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.52 ms: 1.10x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 677 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.62 ms: 1.10x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.4 ms: 1.10x faster                                                 |
| sympy_str                  | 292 ms                                                 | 266 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 409 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.02 ms: 1.09x faster                                                 |
| nqueens                    | 80.1 ms                                                | 73.3 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 46.5 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 50.4 ms: 1.06x faster                                                 |
| django_template            | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.30 sec: 1.05x faster                                                |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| meteor_contest             | 104 ms                                                 | 99.1 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 81.6 ms: 1.04x faster                                                 |
| sympy_expand               | 468 ms                                                 | 449 ms: 1.04x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 56.8 ms: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 76.1 ms: 1.04x faster                                                 |
| nbody                      | 89.3 ms                                                | 86.4 ms: 1.03x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 369 ms: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                 | 189 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                 |
| telco                      | 6.53 ms                                                | 7.24 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.2 ms: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.17x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.80 ms: 1.39x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 276 ms: 2.59x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (3): json, pickle_pure_python, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250226-3.14.0a5+-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.12x