# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 45cd786
- commit date: 2025-04-08
- overall geometric mean: 1.032x slower
- HPT reliability: 98.28%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 287 ms: 1.11x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 69.2 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 535 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 556 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.43x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 292 ms: 1.40x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 265 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 479 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 504 ms: 1.32x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.30x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.5 ms: 1.09x faster                                                 |
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                                  |
| nbody          | 85.3 ms                                                                | 118 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.93 ms: 1.10x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.05x faster                                                  |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.3 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.21 sec: 1.10x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 94.8 ms: 1.11x slower                                                 |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 238 us: 1.14x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.3 ms: 1.15x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 344 us: 1.18x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.9 ms: 1.18x slower                                                 |
| django_template | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.0 ms: 1.24x slower                                                 |
| mako            | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.87x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.35 sec: 1.73x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 535 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 556 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.43x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 292 ms: 1.40x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 265 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 479 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 504 ms: 1.32x faster                                                  |
| deepcopy                   | 357 us                                                                 | 297 us: 1.20x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.93 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.3 ms: 1.09x faster                                                 |
| float                      | 76.7 ms                                                                | 70.5 ms: 1.09x faster                                                 |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| go                         | 141 ms                                                                 | 133 ms: 1.06x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.98 us: 1.05x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 128 ms: 1.04x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.6 us: 1.04x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.03x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 73.1 ms: 1.02x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 351 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 69.2 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.03x slower                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.61 sec: 1.04x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.75 sec: 1.05x slower                                                |
| json                       | 4.98 ms                                                                | 5.22 ms: 1.05x slower                                                 |
| pyflate                    | 449 ms                                                                 | 474 ms: 1.05x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.09 ms: 1.07x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.41 ms: 1.08x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.21 sec: 1.10x slower                                                |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 790 ms: 1.10x slower                                                  |
| 2to3                       | 259 ms                                                                 | 287 ms: 1.11x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.7 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 94.8 ms: 1.11x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.13x slower                                                |
| chaos                      | 56.3 ms                                                                | 63.9 ms: 1.13x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 88.2 ms: 1.13x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 238 us: 1.14x slower                                                  |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 68.3 ms: 1.15x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.5 ms: 1.16x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.9 ms: 1.16x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 344 us: 1.18x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 57.9 ms: 1.18x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.25 us: 1.18x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.20 us: 1.19x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.07 ms: 1.19x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 134 ms: 1.19x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 542 ms: 1.19x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 327 ms: 1.19x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.72 ms: 1.20x slower                                                 |
| richards_super             | 50.4 ms                                                                | 61.0 ms: 1.21x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.8 ms: 1.21x slower                                                 |
| raytrace                   | 250 ms                                                                 | 303 ms: 1.21x slower                                                  |
| comprehensions             | 16.6 us                                                                | 20.2 us: 1.22x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 462 ms: 1.23x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 27.0 ms: 1.24x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 194 us: 1.25x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.2 ms: 1.25x slower                                                 |
| coverage                   | 82.5 ms                                                                | 107 ms: 1.30x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                 |
| nbody                      | 85.3 ms                                                                | 118 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.15 ms: 3.41x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 96.0 ms: 8.73x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): pylint, create_gc_cycles
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a7+-45cd786-NOGIL/bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x slower

# HPT report

- Reliability score: 98.28% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x