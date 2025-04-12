# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_nolock
- machine: linux-x86_64
- commit hash: 4f84be5
- commit date: 2025-04-12
- overall geometric mean: 1.012x slower
- HPT reliability: 91.36%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 280 ms: 1.08x slower                                        |
| docutils       | 2.63 sec                                                               | 2.68 sec: 1.02x slower                                      |
| html5lib       | 68.6 ms                                                                | 64.7 ms: 1.06x faster                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 520 ms: 1.73x faster                                        |
| async_tree_io              | 881 ms                                                                 | 547 ms: 1.61x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.48x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.47x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 283 ms: 1.45x faster                                        |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.38x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 550 ms: 1.21x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 523 ms: 1.21x faster                                        |
| async_generators           | 375 ms                                                                 | 361 ms: 1.04x faster                                        |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                       |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                        |
| Geometric mean             | (ref)                                                                  | 1.31x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.5 ms: 1.14x faster                                       |
| pidigits       | 216 ms                                                                 | 203 ms: 1.07x faster                                        |
| nbody          | 85.3 ms                                                                | 110 ms: 1.28x slower                                        |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                       |
| regex_v8       | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                       |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                        |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                        |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.0 ms: 1.08x faster                                       |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                        |
| tomli_loads          | 2.01 sec                                                               | 2.10 sec: 1.04x slower                                      |
| xml_etree_generate   | 85.4 ms                                                                | 93.0 ms: 1.09x slower                                       |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                        |
| json_loads           | 27.3 us                                                                | 30.6 us: 1.12x slower                                       |
| xml_etree_process    | 59.2 ms                                                                | 66.4 ms: 1.12x slower                                       |
| pickle_pure_python   | 292 us                                                                 | 329 us: 1.13x slower                                        |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.44x slower                                       |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.4 ms: 1.13x slower                                       |
| django_template | 34.2 ms                                                                | 39.5 ms: 1.16x slower                                       |
| genshi_text     | 21.7 ms                                                                | 25.7 ms: 1.18x slower                                       |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.88x faster                                       |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                      |
| async_tree_io_tg           | 901 ms                                                                 | 520 ms: 1.73x faster                                        |
| async_tree_io              | 881 ms                                                                 | 547 ms: 1.61x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.48x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.47x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 283 ms: 1.45x faster                                        |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.38x faster                                        |
| deepcopy                   | 357 us                                                                 | 286 us: 1.25x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 550 ms: 1.21x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 523 ms: 1.21x faster                                        |
| regex_effbot               | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                       |
| float                      | 76.7 ms                                                                | 67.5 ms: 1.14x faster                                       |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                       |
| go                         | 141 ms                                                                 | 126 ms: 1.11x faster                                        |
| regex_v8                   | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                       |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.0 ms: 1.08x faster                                       |
| deepcopy_memo              | 38.1 us                                                                | 35.1 us: 1.08x faster                                       |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.08x faster                                        |
| pidigits                   | 216 ms                                                                 | 203 ms: 1.07x faster                                        |
| html5lib                   | 68.6 ms                                                                | 64.7 ms: 1.06x faster                                       |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                        |
| dulwich_log                | 74.5 ms                                                                | 70.6 ms: 1.05x faster                                       |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.05x faster                                        |
| deepcopy_reduce            | 3.12 us                                                                | 2.97 us: 1.05x faster                                       |
| async_generators           | 375 ms                                                                 | 361 ms: 1.04x faster                                        |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.03x faster                                        |
| scimark_fft                | 348 ms                                                                 | 343 ms: 1.02x faster                                        |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                       |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.00x faster                                      |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                        |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                       |
| bpe_tokeniser              | 4.46 sec                                                               | 4.49 sec: 1.01x slower                                      |
| docutils                   | 2.63 sec                                                               | 2.68 sec: 1.02x slower                                      |
| tomli_loads                | 2.01 sec                                                               | 2.10 sec: 1.04x slower                                      |
| pyflate                    | 449 ms                                                                 | 470 ms: 1.05x slower                                        |
| json                       | 4.98 ms                                                                | 5.21 ms: 1.05x slower                                       |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.02 ms: 1.06x slower                                       |
| logging_silent             | 98.2 ns                                                                | 105 ns: 1.07x slower                                        |
| pprint_safe_repr           | 719 ms                                                                 | 769 ms: 1.07x slower                                        |
| 2to3                       | 259 ms                                                                 | 280 ms: 1.08x slower                                        |
| telco                      | 7.77 ms                                                                | 8.44 ms: 1.09x slower                                       |
| xml_etree_generate         | 85.4 ms                                                                | 93.0 ms: 1.09x slower                                       |
| pprint_pformat             | 1.46 sec                                                               | 1.59 sec: 1.09x slower                                      |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                        |
| chaos                      | 56.3 ms                                                                | 61.7 ms: 1.10x slower                                       |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                        |
| generators                 | 28.5 ms                                                                | 31.6 ms: 1.11x slower                                       |
| nqueens                    | 77.7 ms                                                                | 86.8 ms: 1.12x slower                                       |
| json_loads                 | 27.3 us                                                                | 30.6 us: 1.12x slower                                       |
| xml_etree_process          | 59.2 ms                                                                | 66.4 ms: 1.12x slower                                       |
| hexiom                     | 5.95 ms                                                                | 6.68 ms: 1.12x slower                                       |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                       |
| pickle_pure_python         | 292 us                                                                 | 329 us: 1.13x slower                                        |
| genshi_xml                 | 49.1 ms                                                                | 55.4 ms: 1.13x slower                                       |
| scimark_monte_carlo        | 65.8 ms                                                                | 74.5 ms: 1.13x slower                                       |
| logging_format             | 6.92 us                                                                | 7.86 us: 1.14x slower                                       |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.14x slower                                        |
| richards                   | 44.4 ms                                                                | 50.7 ms: 1.14x slower                                       |
| logging_simple             | 6.14 us                                                                | 7.03 us: 1.14x slower                                       |
| raytrace                   | 250 ms                                                                 | 288 ms: 1.15x slower                                        |
| django_template            | 34.2 ms                                                                | 39.5 ms: 1.16x slower                                       |
| deltablue                  | 3.10 ms                                                                | 3.58 ms: 1.16x slower                                       |
| sympy_expand               | 454 ms                                                                 | 525 ms: 1.16x slower                                        |
| sympy_str                  | 274 ms                                                                 | 317 ms: 1.16x slower                                        |
| sympy_sum                  | 154 ms                                                                 | 179 ms: 1.16x slower                                        |
| richards_super             | 50.4 ms                                                                | 59.1 ms: 1.17x slower                                       |
| comprehensions             | 16.6 us                                                                | 19.5 us: 1.17x slower                                       |
| genshi_text                | 21.7 ms                                                                | 25.7 ms: 1.18x slower                                       |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                       |
| fannkuch                   | 376 ms                                                                 | 455 ms: 1.21x slower                                        |
| crypto_pyaes               | 68.2 ms                                                                | 82.7 ms: 1.21x slower                                       |
| typing_runtime_protocols   | 156 us                                                                 | 189 us: 1.21x slower                                        |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                        |
| nbody                      | 85.3 ms                                                                | 110 ms: 1.28x slower                                        |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                        |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                       |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.44x slower                                       |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                       |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                       |
| bench_mp_pool              | 11.0 ms                                                                | 95.4 ms: 8.67x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                |

Benchmark hidden because not significant (2): pylint, create_gc_cycles
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250412-3.14.0a7+-4f84be5-NOGIL/bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 91.36% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x