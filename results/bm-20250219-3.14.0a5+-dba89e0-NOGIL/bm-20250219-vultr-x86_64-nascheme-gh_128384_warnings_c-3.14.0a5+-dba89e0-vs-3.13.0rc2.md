# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_128384_warnings_c
- machine: linux-x86_64
- commit hash: dba89e0
- commit date: 2025-02-19
- overall geometric mean: 1.081x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 307 ms: 1.18x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                   |
| html5lib       | 68.6 ms                                                                | 71.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 593 ms: 1.52x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 319 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 292 ms: 1.21x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                                     |
| float          | 76.7 ms                                                                | 75.5 ms: 1.02x faster                                                    |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.75 ms: 1.17x faster                                                    |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 23.8 ms: 1.02x slower                                                    |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.15x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                                    |
| json_loads           | 27.3 us                                                                | 31.6 us: 1.16x slower                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.34 sec: 1.17x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                    |
| pickle_pure_python   | 292 us                                                                 | 365 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                    |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                                    |
| django_template | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                                    |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.39x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.76 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 593 ms: 1.52x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 319 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 292 ms: 1.21x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.75 ms: 1.17x faster                                                    |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                    |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                     |
| float                      | 76.7 ms                                                                | 75.5 ms: 1.02x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 3.18 us: 1.02x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                     |
| regex_v8                   | 23.2 ms                                                                | 23.8 ms: 1.02x slower                                                    |
| html5lib                   | 68.6 ms                                                                | 71.3 ms: 1.04x slower                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.70 sec: 1.05x slower                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.41 ms: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.06x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                   |
| json                       | 4.98 ms                                                                | 5.43 ms: 1.09x slower                                                    |
| scimark_fft                | 348 ms                                                                 | 383 ms: 1.10x slower                                                     |
| telco                      | 7.77 ms                                                                | 8.55 ms: 1.10x slower                                                    |
| pyflate                    | 449 ms                                                                 | 495 ms: 1.10x slower                                                     |
| dulwich_log                | 74.5 ms                                                                | 82.5 ms: 1.11x slower                                                    |
| generators                 | 28.5 ms                                                                | 31.7 ms: 1.11x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 811 ms: 1.13x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                                    |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.13x slower                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.47 ms: 1.15x slower                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.15x slower                                                   |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.15x slower                                                     |
| json_loads                 | 27.3 us                                                                | 31.6 us: 1.16x slower                                                    |
| thrift                     | 772 us                                                                 | 893 us: 1.16x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                                | 60.9 ms: 1.16x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.34 sec: 1.17x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                                    |
| coverage                   | 82.5 ms                                                                | 96.3 ms: 1.17x slower                                                    |
| logging_simple             | 6.14 us                                                                | 7.19 us: 1.17x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                     |
| 2to3                       | 259 ms                                                                 | 307 ms: 1.18x slower                                                     |
| mdp                        | 2.34 sec                                                               | 2.78 sec: 1.19x slower                                                   |
| comprehensions             | 16.6 us                                                                | 19.7 us: 1.19x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                                     |
| logging_format             | 6.92 us                                                                | 8.31 us: 1.20x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 136 ms: 1.21x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 551 ms: 1.22x slower                                                     |
| sqlglot_transpile          | 1.55 ms                                                                | 1.89 ms: 1.22x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 24.1 ms: 1.22x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                     |
| django_template            | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                                    |
| nqueens                    | 77.7 ms                                                                | 95.8 ms: 1.23x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 7.44 ms: 1.25x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 365 us: 1.25x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                                | 1.57 ms: 1.26x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.9 ms: 1.26x slower                                                    |
| chaos                      | 56.3 ms                                                                | 70.9 ms: 1.26x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 87.4 ms: 1.28x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                                    |
| richards                   | 44.4 ms                                                                | 57.2 ms: 1.29x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 489 ms: 1.30x slower                                                     |
| richards_super             | 50.4 ms                                                                | 66.1 ms: 1.31x slower                                                    |
| raytrace                   | 250 ms                                                                 | 334 ms: 1.34x slower                                                     |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.39x slower                                                    |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 4.75 ms: 1.53x slower                                                    |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.38 ms: 3.65x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 94.7 ms: 8.61x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                             |

Benchmark hidden because not significant (7): asyncio_websockets, pylint, deepcopy_memo, pathlib, go, async_generators, scimark_sor
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-dba89e0-NOGIL/bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x