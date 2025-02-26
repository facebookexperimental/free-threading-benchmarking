# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: b10c3be
- commit date: 2025-02-26
- overall geometric mean: 1.055x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.15x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 70.9 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 579 ms: 1.52x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                                  |
| float          | 76.7 ms                                                                | 70.6 ms: 1.09x faster                                                 |
| nbody          | 85.3 ms                                                                | 122 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.03x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 24.3 ms: 1.05x slower                                                 |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 96.4 ms: 1.13x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 241 us: 1.16x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.9 ms: 1.18x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 347 us: 1.19x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.7 ms: 1.18x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.9 ms: 1.24x slower                                                 |
| django_template | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                                 |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.26x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 579 ms: 1.52x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                  |
| deepcopy                   | 357 us                                                                 | 300 us: 1.19x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.05 us: 1.10x faster                                                 |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                                  |
| float                      | 76.7 ms                                                                | 70.6 ms: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                                 |
| go                         | 141 ms                                                                 | 132 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 127 ms: 1.05x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.7 us: 1.04x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.03x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                 |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.08 us: 1.01x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.01x faster                                                  |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.02x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 70.9 ms: 1.03x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 361 ms: 1.04x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.65 sec: 1.04x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                |
| regex_v8                   | 23.2 ms                                                                | 24.3 ms: 1.05x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| pyflate                    | 449 ms                                                                 | 474 ms: 1.06x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.12 ms: 1.08x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.55 ms: 1.10x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 83.2 ms: 1.12x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 804 ms: 1.12x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 119 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 96.4 ms: 1.13x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                                |
| thrift                     | 772 us                                                                 | 878 us: 1.14x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.66 sec: 1.14x slower                                                |
| generators                 | 28.5 ms                                                                | 32.5 ms: 1.14x slower                                                 |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 60.5 ms: 1.15x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 241 us: 1.16x slower                                                  |
| coverage                   | 82.5 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.16x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.73 sec: 1.17x slower                                                |
| logging_format             | 6.92 us                                                                | 8.11 us: 1.17x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.5 us: 1.17x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.22 us: 1.18x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.7 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.4 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.9 ms: 1.18x slower                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.84 ms: 1.18x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.67 ms: 1.19x slower                                                 |
| chaos                      | 56.3 ms                                                                | 66.9 ms: 1.19x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 347 us: 1.19x slower                                                  |
| richards                   | 44.4 ms                                                                | 53.1 ms: 1.19x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.8 ms: 1.21x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 548 ms: 1.21x slower                                                  |
| raytrace                   | 250 ms                                                                 | 302 ms: 1.21x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 136 ms: 1.21x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.22 ms: 1.21x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 94.4 ms: 1.21x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.51 ms: 1.21x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                  |
| richards_super             | 50.4 ms                                                                | 61.6 ms: 1.22x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 26.9 ms: 1.24x slower                                                 |
| django_template            | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 466 ms: 1.24x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.1 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 122 ms: 1.42x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.29 ms: 3.56x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.7 ms: 8.61x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, coroutines
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250226-3.14.0a5+-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.055x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x