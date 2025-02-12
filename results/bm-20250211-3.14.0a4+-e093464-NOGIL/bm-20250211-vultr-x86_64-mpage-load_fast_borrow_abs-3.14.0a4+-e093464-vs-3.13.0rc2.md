# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: e093464
- commit date: 2025-02-11
- overall geometric mean: 1.070x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 301 ms: 1.16x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.81 sec: 1.07x slower                                                |
| html5lib       | 67.0 ms                                                      | 71.9 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 500 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                  |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                  |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 71.8 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 124 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                 |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                 |
| regex_compile  | 132 ms                                                       | 150 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.8 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                |
| json_loads           | 27.0 us                                                      | 31.3 us: 1.16x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 247 us: 1.18x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 364 us: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.7 ms: 1.20x slower                                                 |
| django_template | 34.1 ms                                                      | 42.7 ms: 1.25x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.4 ms: 1.27x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.74 ms: 1.81x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 500 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                  |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                  |
| deepcopy                   | 355 us                                                       | 303 us: 1.17x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                 |
| float                      | 77.5 ms                                                      | 71.8 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.8 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 36.7 us: 1.06x faster                                                 |
| go                         | 141 ms                                                       | 137 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                 |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                  |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.17 us: 1.02x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.02x slower                                                 |
| scimark_fft                | 349 ms                                                       | 360 ms: 1.03x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.66 sec: 1.05x slower                                                |
| telco                      | 7.82 ms                                                      | 8.28 ms: 1.06x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.20 sec: 1.07x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.81 sec: 1.07x slower                                                |
| html5lib                   | 67.0 ms                                                      | 71.9 ms: 1.07x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 797 ms: 1.08x slower                                                  |
| logging_silent             | 103 ns                                                       | 111 ns: 1.08x slower                                                  |
| json                       | 4.93 ms                                                      | 5.37 ms: 1.09x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.64 sec: 1.10x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.17 ms: 1.10x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 82.5 ms: 1.10x slower                                                 |
| pyflate                    | 449 ms                                                       | 496 ms: 1.11x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.63 sec: 1.12x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.13x slower                                                  |
| regex_compile              | 132 ms                                                       | 150 ms: 1.14x slower                                                  |
| thrift                     | 778 us                                                       | 891 us: 1.15x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                 |
| 2to3                       | 260 ms                                                       | 301 ms: 1.16x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.3 us: 1.16x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 247 us: 1.18x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.27 us: 1.18x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.86 ms: 1.19x slower                                                 |
| coverage                   | 83.0 ms                                                      | 99.0 ms: 1.19x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 135 ms: 1.20x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.7 ms: 1.20x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 23.9 ms: 1.21x slower                                                 |
| sympy_expand               | 457 ms                                                       | 552 ms: 1.21x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.29 us: 1.21x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                 |
| chaos                      | 57.3 ms                                                      | 69.7 ms: 1.22x slower                                                 |
| comprehensions             | 16.5 us                                                      | 20.0 us: 1.22x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.5 ms: 1.22x slower                                                 |
| richards                   | 45.2 ms                                                      | 55.1 ms: 1.22x slower                                                 |
| sympy_str                  | 275 ms                                                       | 335 ms: 1.22x slower                                                  |
| generators                 | 28.8 ms                                                      | 35.2 ms: 1.22x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 96.4 ms: 1.23x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.54 ms: 1.23x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.39 ms: 1.23x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 364 us: 1.24x slower                                                  |
| richards_super             | 51.6 ms                                                      | 64.1 ms: 1.24x slower                                                 |
| django_template            | 34.1 ms                                                      | 42.7 ms: 1.25x slower                                                 |
| raytrace                   | 253 ms                                                       | 318 ms: 1.26x slower                                                  |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 27.4 ms: 1.27x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 86.6 ms: 1.27x slower                                                 |
| fannkuch                   | 370 ms                                                       | 473 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 203 us: 1.31x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.40x slower                                                 |
| nbody                      | 85.1 ms                                                      | 124 ms: 1.46x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.64 ms: 1.49x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.29 ms: 3.58x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 93.2 ms: 8.48x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250211-3.14.0a4+-e093464-NOGIL/bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.070x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x