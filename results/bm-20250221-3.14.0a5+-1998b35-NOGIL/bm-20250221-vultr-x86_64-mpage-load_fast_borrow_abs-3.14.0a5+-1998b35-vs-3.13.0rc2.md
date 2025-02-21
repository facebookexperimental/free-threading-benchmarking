# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 1998b35
- commit date: 2025-02-21
- overall geometric mean: 1.031x slower
- HPT reliability: 99.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 287 ms: 1.10x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.72 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 67.1 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 528 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 557 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.47x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 325 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 293 ms: 1.40x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 265 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 527 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 559 ms: 1.19x faster                                                  |
| async_generators           | 375 ms                                                                 | 360 ms: 1.04x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.5 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 68.9 ms: 1.11x faster                                                 |
| pidigits       | 216 ms                                                                 | 240 ms: 1.11x slower                                                  |
| nbody          | 85.3 ms                                                                | 114 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                 |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                                 |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 85.6 ms: 1.10x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.09 sec: 1.04x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 92.4 ms: 1.08x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 66.4 ms: 1.12x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 330 us: 1.13x slower                                                  |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.65 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.7 ms: 1.13x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 25.3 ms: 1.16x slower                                                 |
| django_template | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                 |
| mako            | 11.2 ms                                                                | 15.1 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.89x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 528 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 557 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.47x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 325 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 293 ms: 1.40x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 265 ms: 1.33x faster                                                  |
| deepcopy                   | 357 us                                                                 | 292 us: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 527 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 559 ms: 1.19x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                 |
| go                         | 141 ms                                                                 | 123 ms: 1.14x faster                                                  |
| float                      | 76.7 ms                                                                | 68.9 ms: 1.11x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.11x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 85.6 ms: 1.10x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.9 us: 1.09x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| async_generators           | 375 ms                                                                 | 360 ms: 1.04x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.5 ms: 1.04x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.04x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 67.1 ms: 1.02x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.09 us: 1.01x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                                 |
| pyflate                    | 449 ms                                                                 | 452 ms: 1.01x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.48 sec: 1.01x slower                                                |
| scimark_fft                | 348 ms                                                                 | 351 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.72 sec: 1.03x slower                                                |
| generators                 | 28.5 ms                                                                | 29.6 ms: 1.04x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.09 sec: 1.04x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 761 ms: 1.06x slower                                                  |
| json                       | 4.98 ms                                                                | 5.28 ms: 1.06x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 105 ns: 1.07x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.11 ms: 1.08x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.57 sec: 1.08x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 92.4 ms: 1.08x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 115 ms: 1.09x slower                                                  |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.09x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 81.6 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| 2to3                       | 259 ms                                                                 | 287 ms: 1.10x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.59 ms: 1.10x slower                                                 |
| pidigits                   | 216 ms                                                                 | 240 ms: 1.11x slower                                                  |
| richards                   | 44.4 ms                                                                | 49.5 ms: 1.11x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 58.7 ms: 1.11x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 66.4 ms: 1.12x slower                                                 |
| comprehensions             | 16.6 us                                                                | 18.6 us: 1.12x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.48 ms: 1.12x slower                                                 |
| chaos                      | 56.3 ms                                                                | 63.5 ms: 1.13x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 74.3 ms: 1.13x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 330 us: 1.13x slower                                                  |
| thrift                     | 772 us                                                                 | 873 us: 1.13x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.96 us: 1.13x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 55.7 ms: 1.13x slower                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.78 ms: 1.14x slower                                                 |
| richards_super             | 50.4 ms                                                                | 57.7 ms: 1.15x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.82 ms: 1.15x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.96 us: 1.15x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.70 sec: 1.15x slower                                                |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| raytrace                   | 250 ms                                                                 | 290 ms: 1.16x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.16x slower                                                  |
| coverage                   | 82.5 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 25.3 ms: 1.16x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 529 ms: 1.17x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 91.0 ms: 1.17x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 321 ms: 1.17x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.1 ms: 1.17x slower                                                 |
| django_template            | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.47 ms: 1.18x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 182 ms: 1.18x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 455 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 190 us: 1.22x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 83.4 ms: 1.22x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 125 ms: 1.24x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.65 ms: 1.30x slower                                                 |
| nbody                      | 85.3 ms                                                                | 114 ms: 1.33x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.1 ms: 1.35x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.26 ms: 3.53x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 95.1 ms: 8.65x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (4): pylint, pathlib, asyncio_websockets, create_gc_cycles
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250221-3.14.0a5+-1998b35-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 99.75% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x