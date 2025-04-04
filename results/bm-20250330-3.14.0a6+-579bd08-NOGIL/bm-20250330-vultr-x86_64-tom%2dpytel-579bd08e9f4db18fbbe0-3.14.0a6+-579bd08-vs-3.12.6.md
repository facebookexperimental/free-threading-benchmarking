# Results vs. 3.12.6

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.046x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                                        |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                      |
| html5lib       | 63.6 ms                                                | 71.3 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.02x faster                                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                        |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                        |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                        |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                        |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 523 ms: 1.37x faster                                                        |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                        |
| async_generators           | 384 ms                                                 | 386 ms: 1.00x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                       |
| pidigits       | 184 ms                                                 | 223 ms: 1.21x slower                                                        |
| nbody          | 89.3 ms                                                | 135 ms: 1.51x slower                                                        |
| Geometric mean | (ref)                                                  | 1.21x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                       |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                       |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                        |
| regex_compile  | 142 ms                                                 | 157 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                       |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                        |
| json_loads           | 26.5 us                                                | 28.8 us: 1.08x slower                                                       |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 97.6 ms: 1.15x slower                                                       |
| unpickle_pure_python | 221 us                                                 | 257 us: 1.17x slower                                                        |
| pickle_pure_python   | 308 us                                                 | 361 us: 1.17x slower                                                        |
| xml_etree_process    | 59.0 ms                                                | 70.8 ms: 1.20x slower                                                       |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                       |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.3 ms: 1.18x slower                                                       |
| genshi_text     | 22.8 ms                                                | 28.2 ms: 1.24x slower                                                       |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                       |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.02x faster                                                        |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                        |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                        |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                        |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                        |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 523 ms: 1.37x faster                                                        |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                       |
| deepcopy                   | 352 us                                                 | 311 us: 1.13x faster                                                        |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                       |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                       |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                       |
| dulwich_log                | 78.9 ms                                                | 72.8 ms: 1.08x faster                                                       |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                        |
| float                      | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                       |
| deepcopy_memo              | 40.3 us                                                | 39.1 us: 1.03x faster                                                       |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                                       |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                        |
| async_generators           | 384 ms                                                 | 386 ms: 1.00x slower                                                        |
| deepcopy_reduce            | 3.08 us                                                | 3.13 us: 1.02x slower                                                       |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.87 sec: 1.03x slower                                                      |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                        |
| go                         | 139 ms                                                 | 144 ms: 1.04x slower                                                        |
| comprehensions             | 19.8 us                                                | 20.8 us: 1.05x slower                                                       |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                      |
| scimark_sor                | 130 ms                                                 | 137 ms: 1.06x slower                                                        |
| logging_silent             | 109 ns                                                 | 116 ns: 1.06x slower                                                        |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.5 ms: 1.08x slower                                                       |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.08x slower                                                       |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                        |
| logging_simple             | 6.63 us                                                | 7.22 us: 1.09x slower                                                       |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                                        |
| chaos                      | 62.8 ms                                                | 68.6 ms: 1.09x slower                                                       |
| thrift                     | 791 us                                                 | 868 us: 1.10x slower                                                        |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                        |
| regex_compile              | 142 ms                                                 | 157 ms: 1.10x slower                                                        |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                                        |
| logging_format             | 7.35 us                                                | 8.22 us: 1.12x slower                                                       |
| pyflate                    | 448 ms                                                 | 501 ms: 1.12x slower                                                        |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                      |
| html5lib                   | 63.6 ms                                                | 71.3 ms: 1.12x slower                                                       |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                                        |
| deltablue                  | 3.45 ms                                                | 3.91 ms: 1.13x slower                                                       |
| pprint_safe_repr           | 743 ms                                                 | 851 ms: 1.15x slower                                                        |
| xml_etree_generate         | 85.2 ms                                                | 97.6 ms: 1.15x slower                                                       |
| sympy_integrate            | 20.5 ms                                                | 23.6 ms: 1.15x slower                                                       |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                        |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                      |
| unpickle_pure_python       | 221 us                                                 | 257 us: 1.17x slower                                                        |
| scimark_fft                | 342 ms                                                 | 399 ms: 1.17x slower                                                        |
| pickle_pure_python         | 308 us                                                 | 361 us: 1.17x slower                                                        |
| crypto_pyaes               | 76.6 ms                                                | 90.0 ms: 1.18x slower                                                       |
| genshi_xml                 | 50.2 ms                                                | 59.3 ms: 1.18x slower                                                       |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                                        |
| richards                   | 45.9 ms                                                | 54.8 ms: 1.19x slower                                                       |
| xml_etree_process          | 59.0 ms                                                | 70.8 ms: 1.20x slower                                                       |
| pidigits                   | 184 ms                                                 | 223 ms: 1.21x slower                                                        |
| nqueens                    | 80.1 ms                                                | 98.0 ms: 1.22x slower                                                       |
| richards_super             | 51.9 ms                                                | 63.8 ms: 1.23x slower                                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 84.5 ms: 1.24x slower                                                       |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                       |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                       |
| genshi_text                | 22.8 ms                                                | 28.2 ms: 1.24x slower                                                       |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                        |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                       |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                        |
| hexiom                     | 6.17 ms                                                | 7.75 ms: 1.26x slower                                                       |
| scimark_lu                 | 114 ms                                                 | 144 ms: 1.26x slower                                                        |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.71 ms: 1.30x slower                                                       |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                                        |
| telco                      | 6.53 ms                                                | 8.95 ms: 1.37x slower                                                       |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                       |
| nbody                      | 89.3 ms                                                | 135 ms: 1.51x slower                                                        |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                        |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                       |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                       |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                       |
| bench_mp_pool              | 10.8 ms                                                | 96.6 ms: 8.95x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                                |

Benchmark hidden because not significant (2): pylint, json
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250330-3.14.0a6+-579bd08-NOGIL/bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x