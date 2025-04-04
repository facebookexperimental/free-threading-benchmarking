# Results vs. 3.13.0rc2

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.078x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.15x slower                                                        |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                      |
| html5lib       | 68.6 ms                                                                | 71.3 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                        |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                        |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                        |
| async_tree_memoization     | 459 ms                                                                 | 333 ms: 1.38x faster                                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                        |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                        |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                       |
| async_generators           | 375 ms                                                                 | 386 ms: 1.03x slower                                                        |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 77.7 ms: 1.01x slower                                                       |
| pidigits       | 216 ms                                                                 | 223 ms: 1.03x slower                                                        |
| nbody          | 85.3 ms                                                                | 135 ms: 1.58x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                       |
| regex_v8       | 23.2 ms                                                                | 22.0 ms: 1.06x faster                                                       |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.03x faster                                                        |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.19x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                       |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                        |
| json_loads           | 27.3 us                                                                | 28.8 us: 1.05x slower                                                       |
| xml_etree_generate   | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                                       |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 70.8 ms: 1.19x slower                                                       |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                       |
| unpickle_pure_python | 208 us                                                                 | 257 us: 1.24x slower                                                        |
| pickle_pure_python   | 292 us                                                                 | 361 us: 1.24x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                       |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                                       |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                                       |
| django_template | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                       |
| genshi_text     | 21.7 ms                                                                | 28.2 ms: 1.30x slower                                                       |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                                       |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.86x faster                                                       |
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                        |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                        |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                        |
| async_tree_memoization     | 459 ms                                                                 | 333 ms: 1.38x faster                                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                        |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                        |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                       |
| deepcopy                   | 357 us                                                                 | 311 us: 1.15x faster                                                        |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                       |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                       |
| regex_v8                   | 23.2 ms                                                                | 22.0 ms: 1.06x faster                                                       |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                        |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.03x faster                                                        |
| dulwich_log                | 74.5 ms                                                                | 72.8 ms: 1.02x faster                                                       |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                       |
| float                      | 76.7 ms                                                                | 77.7 ms: 1.01x slower                                                       |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                       |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                                       |
| deepcopy_memo              | 38.1 us                                                                | 39.1 us: 1.03x slower                                                       |
| go                         | 141 ms                                                                 | 144 ms: 1.03x slower                                                        |
| scimark_sor                | 134 ms                                                                 | 137 ms: 1.03x slower                                                        |
| pidigits                   | 216 ms                                                                 | 223 ms: 1.03x slower                                                        |
| async_generators           | 375 ms                                                                 | 386 ms: 1.03x slower                                                        |
| html5lib                   | 68.6 ms                                                                | 71.3 ms: 1.04x slower                                                       |
| json_loads                 | 27.3 us                                                                | 28.8 us: 1.05x slower                                                       |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                      |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                        |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.87 sec: 1.09x slower                                                      |
| pyflate                    | 449 ms                                                                 | 501 ms: 1.12x slower                                                        |
| generators                 | 28.5 ms                                                                | 32.0 ms: 1.12x slower                                                       |
| thrift                     | 772 us                                                                 | 868 us: 1.12x slower                                                        |
| xml_etree_generate         | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                                       |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.15x slower                                                        |
| scimark_fft                | 348 ms                                                                 | 399 ms: 1.15x slower                                                        |
| telco                      | 7.77 ms                                                                | 8.95 ms: 1.15x slower                                                       |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                                      |
| logging_simple             | 6.14 us                                                                | 7.22 us: 1.18x slower                                                       |
| logging_silent             | 98.2 ns                                                                | 116 ns: 1.18x slower                                                        |
| pprint_safe_repr           | 719 ms                                                                 | 851 ms: 1.18x slower                                                        |
| logging_format             | 6.92 us                                                                | 8.22 us: 1.19x slower                                                       |
| mdp                        | 2.34 sec                                                               | 2.79 sec: 1.19x slower                                                      |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.19x slower                                                        |
| xml_etree_process          | 59.2 ms                                                                | 70.8 ms: 1.19x slower                                                       |
| sympy_integrate            | 19.7 ms                                                                | 23.6 ms: 1.20x slower                                                       |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                        |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.71 ms: 1.20x slower                                                       |
| pprint_pformat             | 1.46 sec                                                               | 1.75 sec: 1.20x slower                                                      |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                       |
| genshi_xml                 | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                                       |
| sympy_expand               | 454 ms                                                                 | 552 ms: 1.22x slower                                                        |
| chaos                      | 56.3 ms                                                                | 68.6 ms: 1.22x slower                                                       |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                                        |
| richards                   | 44.4 ms                                                                | 54.8 ms: 1.23x slower                                                       |
| unpickle_pure_python       | 208 us                                                                 | 257 us: 1.24x slower                                                        |
| pickle_pure_python         | 292 us                                                                 | 361 us: 1.24x slower                                                        |
| comprehensions             | 16.6 us                                                                | 20.8 us: 1.26x slower                                                       |
| nqueens                    | 77.7 ms                                                                | 98.0 ms: 1.26x slower                                                       |
| deltablue                  | 3.10 ms                                                                | 3.91 ms: 1.26x slower                                                       |
| richards_super             | 50.4 ms                                                                | 63.8 ms: 1.26x slower                                                       |
| django_template            | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                       |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                        |
| scimark_lu                 | 112 ms                                                                 | 144 ms: 1.28x slower                                                        |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.5 ms: 1.28x slower                                                       |
| genshi_text                | 21.7 ms                                                                | 28.2 ms: 1.30x slower                                                       |
| typing_runtime_protocols   | 156 us                                                                 | 202 us: 1.30x slower                                                        |
| hexiom                     | 5.95 ms                                                                | 7.75 ms: 1.30x slower                                                       |
| fannkuch                   | 376 ms                                                                 | 490 ms: 1.30x slower                                                        |
| raytrace                   | 250 ms                                                                 | 326 ms: 1.30x slower                                                        |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                        |
| crypto_pyaes               | 68.2 ms                                                                | 90.0 ms: 1.32x slower                                                       |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                                       |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                       |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                                       |
| nbody                      | 85.3 ms                                                                | 135 ms: 1.58x slower                                                        |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                       |
| bench_mp_pool              | 11.0 ms                                                                | 96.6 ms: 8.79x slower                                                       |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                                |

Benchmark hidden because not significant (4): pylint, deepcopy_reduce, asyncio_websockets, json
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250330-3.14.0a6+-579bd08-NOGIL/bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x