# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 7fc8bb1
- commit date: 2025-04-08
- overall geometric mean: 1.044x slower
- HPT reliability: 99.47%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 291 ms: 1.12x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 70.5 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 536 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 564 ms: 1.56x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 296 ms: 1.38x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 498 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 528 ms: 1.26x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.1 ms: 1.09x faster                                                 |
| pidigits       | 216 ms                                                                 | 217 ms: 1.00x slower                                                  |
| nbody          | 85.3 ms                                                                | 117 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.71 ms: 1.18x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 183 ms: 1.03x faster                                                  |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| json_loads           | 27.3 us                                                                | 30.7 us: 1.12x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 96.0 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 243 us: 1.17x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 70.2 ms: 1.19x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 350 us: 1.20x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.6 ms: 1.19x slower                                                 |
| django_template | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                                 |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.88x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.37 sec: 1.71x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 536 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 564 ms: 1.56x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 296 ms: 1.38x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 498 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 528 ms: 1.26x faster                                                  |
| deepcopy                   | 357 us                                                                 | 298 us: 1.20x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.71 ms: 1.18x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.13x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                 |
| float                      | 76.7 ms                                                                | 70.1 ms: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 129 ms: 1.04x faster                                                  |
| go                         | 141 ms                                                                 | 136 ms: 1.03x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.8 us: 1.03x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 183 ms: 1.03x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.07 us: 1.02x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 73.3 ms: 1.02x faster                                                 |
| pidigits                   | 216 ms                                                                 | 217 ms: 1.00x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 70.5 ms: 1.03x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 358 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.68 sec: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| json                       | 4.98 ms                                                                | 5.28 ms: 1.06x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.10 ms: 1.07x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.41 ms: 1.08x slower                                                 |
| pyflate                    | 449 ms                                                                 | 486 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 799 ms: 1.11x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                                  |
| 2to3                       | 259 ms                                                                 | 291 ms: 1.12x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.7 us: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 96.0 ms: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.14x slower                                                |
| chaos                      | 56.3 ms                                                                | 64.7 ms: 1.15x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 90.0 ms: 1.16x slower                                                 |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.8 ms: 1.17x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 243 us: 1.17x slower                                                  |
| generators                 | 28.5 ms                                                                | 33.5 ms: 1.17x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.2 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 70.2 ms: 1.19x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.21 us: 1.19x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 134 ms: 1.19x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.32 us: 1.19x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 58.6 ms: 1.19x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 542 ms: 1.19x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 350 us: 1.20x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 330 ms: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.23 ms: 1.21x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                 |
| raytrace                   | 250 ms                                                                 | 307 ms: 1.23x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.80 ms: 1.23x slower                                                 |
| richards                   | 44.4 ms                                                                | 54.6 ms: 1.23x slower                                                 |
| richards_super             | 50.4 ms                                                                | 62.4 ms: 1.24x slower                                                 |
| django_template            | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.6 us: 1.24x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 195 us: 1.25x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 471 ms: 1.25x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 86.0 ms: 1.26x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                                 |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.31x slower                                                  |
| nbody                      | 85.3 ms                                                                | 117 ms: 1.38x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.15 ms: 3.40x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 95.9 ms: 8.72x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (3): create_gc_cycles, pylint, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a7+-7fc8bb1-NOGIL/bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.47% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x