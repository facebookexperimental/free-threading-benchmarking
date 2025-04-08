# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.049x slower
- HPT reliability: 99.69%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                |
| html5lib       | 68.6 ms                                                                | 70.7 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 537 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 567 ms: 1.56x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 325 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 295 ms: 1.39x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 532 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 560 ms: 1.19x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 71.6 ms: 1.07x faster                                                 |
| pidigits       | 216 ms                                                                 | 218 ms: 1.01x slower                                                  |
| nbody          | 85.3 ms                                                                | 123 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                 |
| regex_dna      | 189 ms                                                                 | 183 ms: 1.03x faster                                                  |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.7 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.2 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 95.8 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.26 sec: 1.12x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 245 us: 1.18x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 349 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.5 ms: 1.21x slower                                                 |
| django_template | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                                 |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.86x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.37 sec: 1.71x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 537 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 567 ms: 1.56x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 233 ms: 1.43x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 325 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 295 ms: 1.39x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| deepcopy                   | 357 us                                                                 | 300 us: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 532 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 560 ms: 1.19x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.7 ms: 1.09x faster                                                 |
| float                      | 76.7 ms                                                                | 71.6 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 129 ms: 1.03x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.9 us: 1.03x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 183 ms: 1.03x faster                                                  |
| go                         | 141 ms                                                                 | 137 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.05 us: 1.02x faster                                                 |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 73.2 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.01x faster                                                  |
| pidigits                   | 216 ms                                                                 | 218 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 356 ms: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.11 ms: 1.02x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 70.7 ms: 1.03x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.04x slower                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.68 sec: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.2 us: 1.07x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.41 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.22 ms: 1.10x slower                                                 |
| pyflate                    | 449 ms                                                                 | 494 ms: 1.10x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.8 ms: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.26 sec: 1.12x slower                                                |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.13x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 811 ms: 1.13x slower                                                  |
| 2to3                       | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| chaos                      | 56.3 ms                                                                | 65.4 ms: 1.16x slower                                                 |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.16x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                                |
| nqueens                    | 77.7 ms                                                                | 90.7 ms: 1.17x slower                                                 |
| generators                 | 28.5 ms                                                                | 33.5 ms: 1.17x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.3 ms: 1.17x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 245 us: 1.18x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.3 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 349 us: 1.20x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 135 ms: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 545 ms: 1.20x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 330 ms: 1.20x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.40 us: 1.21x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.37 us: 1.21x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 59.5 ms: 1.21x slower                                                 |
| django_template            | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.27 ms: 1.22x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.3 us: 1.22x slower                                                 |
| raytrace                   | 250 ms                                                                 | 309 ms: 1.24x slower                                                  |
| richards                   | 44.4 ms                                                                | 55.1 ms: 1.24x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 470 ms: 1.25x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                                  |
| richards_super             | 50.4 ms                                                                | 63.4 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 87.1 ms: 1.28x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                                 |
| coverage                   | 82.5 ms                                                                | 107 ms: 1.30x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| nbody                      | 85.3 ms                                                                | 123 ms: 1.44x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.15 ms: 3.41x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 96.3 ms: 8.76x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a6+-09d4621-NOGIL/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.049x slower

# HPT report

- Reliability score: 99.69% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x