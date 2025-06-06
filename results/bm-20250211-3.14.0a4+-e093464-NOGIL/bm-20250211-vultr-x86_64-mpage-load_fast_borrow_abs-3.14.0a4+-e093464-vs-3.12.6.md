# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: e093464
- commit date: 2025-02-11
- overall geometric mean: 1.038x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                  |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.07x slower                                                |
| html5lib       | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 572 ms: 1.94x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.7 ms: 1.13x faster                                                 |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| nbody          | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                 |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                |
| unpickle_pure_python | 221 us                                                 | 243 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 364 us: 1.18x slower                                                  |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.63 ms: 1.35x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.1 ms: 1.18x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.6 ms: 1.21x slower                                                 |
| django_template | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.65 ms: 2.09x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 572 ms: 1.94x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                 |
| deepcopy                   | 352 us                                                 | 304 us: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                 |
| float                      | 80.8 ms                                                | 71.7 ms: 1.13x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.10x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 36.9 us: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| go                         | 139 ms                                                 | 136 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                                |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| scimark_sor                | 130 ms                                                 | 130 ms: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.18 us: 1.03x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 82.5 ms: 1.05x slower                                                 |
| raytrace                   | 299 ms                                                 | 314 ms: 1.05x slower                                                  |
| scimark_fft                | 342 ms                                                 | 359 ms: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.07x slower                                                |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                |
| pyflate                    | 448 ms                                                 | 483 ms: 1.08x slower                                                  |
| generators                 | 32.2 ms                                                | 34.8 ms: 1.08x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 806 ms: 1.08x slower                                                  |
| chaos                      | 62.8 ms                                                | 68.8 ms: 1.09x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                |
| logging_simple             | 6.63 us                                                | 7.29 us: 1.10x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 243 us: 1.10x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.86 ms: 1.11x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                  |
| logging_format             | 7.35 us                                                | 8.21 us: 1.12x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.71 sec: 1.12x slower                                                |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.13x slower                                                 |
| html5lib                   | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                 |
| thrift                     | 791 us                                                 | 900 us: 1.14x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.54 ms: 1.14x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 60.7 ms: 1.14x slower                                                 |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                 |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.7 ms: 1.15x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                                 |
| sympy_expand               | 468 ms                                                 | 546 ms: 1.17x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.14 ms: 1.17x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 134 ms: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.1 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 364 us: 1.18x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                                 |
| nqueens                    | 80.1 ms                                                | 96.3 ms: 1.20x slower                                                 |
| richards                   | 45.9 ms                                                | 55.4 ms: 1.20x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.6 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                  |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                  |
| django_template            | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.4 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 468 ms: 1.26x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                                 |
| telco                      | 6.53 ms                                                | 8.38 ms: 1.28x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.60 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.63 ms: 1.35x slower                                                 |
| nbody                      | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.9 ms: 1.39x slower                                                 |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.29 ms: 3.49x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 93.1 ms: 8.62x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (3): comprehensions, pylint, logging_silent
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250211-3.14.0a4+-e093464-NOGIL/bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.038x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x