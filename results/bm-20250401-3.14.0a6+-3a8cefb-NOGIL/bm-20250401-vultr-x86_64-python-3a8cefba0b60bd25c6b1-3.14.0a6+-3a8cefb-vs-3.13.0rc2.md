# Results vs. 3.13.0rc2

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.112x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 312 ms: 1.20x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.90 sec: 1.11x slower                                                 |
| html5lib       | 68.6 ms                                                                | 76.0 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 570 ms: 1.58x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 601 ms: 1.47x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 344 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 498 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 285 ms: 1.24x faster                                                   |
| async_generators           | 375 ms                                                                 | 392 ms: 1.05x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 26.9 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 215 ms: 1.01x faster                                                   |
| float          | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                                  |
| nbody          | 85.3 ms                                                                | 139 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                  |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.05x faster                                                   |
| regex_compile  | 131 ms                                                                 | 171 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| json_loads           | 27.3 us                                                                | 30.8 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.20x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 13.3 ms: 1.26x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 75.0 ms: 1.27x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.57 sec: 1.28x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 272 us: 1.31x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 387 us: 1.33x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.45x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 45.5 ms: 1.33x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 67.5 ms: 1.37x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 31.7 ms: 1.46x slower                                                  |
| mako            | 11.2 ms                                                                | 16.7 ms: 1.49x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.47 sec: 1.59x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 570 ms: 1.58x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 601 ms: 1.47x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 344 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 498 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 285 ms: 1.24x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                                  |
| deepcopy                   | 357 us                                                                 | 324 us: 1.10x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.09 us: 1.08x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| pidigits                   | 216 ms                                                                 | 215 ms: 1.01x faster                                                   |
| float                      | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                  |
| async_generators           | 375 ms                                                                 | 392 ms: 1.05x slower                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 3.27 us: 1.05x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 78.5 ms: 1.05x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 40.4 us: 1.06x slower                                                  |
| json                       | 4.98 ms                                                                | 5.36 ms: 1.08x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 380 ms: 1.09x slower                                                   |
| go                         | 141 ms                                                                 | 154 ms: 1.09x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.91 sec: 1.10x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 119 ms: 1.10x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.90 sec: 1.11x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 76.0 ms: 1.11x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.26 sec: 1.12x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.8 us: 1.13x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.84 ms: 1.14x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 153 ms: 1.14x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.44 ms: 1.14x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 26.9 ms: 1.15x slower                                                  |
| pyflate                    | 449 ms                                                                 | 531 ms: 1.18x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.20x slower                                                   |
| 2to3                       | 259 ms                                                                 | 312 ms: 1.20x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 880 ms: 1.22x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.5 ms: 1.24x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 13.3 ms: 1.26x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 124 ns: 1.26x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.83 sec: 1.26x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 75.0 ms: 1.27x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.57 sec: 1.28x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.2 ms: 1.28x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 198 ms: 1.29x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 354 ms: 1.29x slower                                                   |
| regex_compile              | 131 ms                                                                 | 171 ms: 1.30x slower                                                   |
| chaos                      | 56.3 ms                                                                | 73.5 ms: 1.31x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 593 ms: 1.31x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 272 us: 1.31x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 102 ms: 1.31x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 133 ms: 1.31x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 206 us: 1.32x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 387 us: 1.33x slower                                                   |
| django_template            | 34.2 ms                                                                | 45.5 ms: 1.33x slower                                                  |
| coverage                   | 82.5 ms                                                                | 111 ms: 1.34x slower                                                   |
| comprehensions             | 16.6 us                                                                | 22.2 us: 1.34x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 91.6 ms: 1.34x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 8.09 ms: 1.36x slower                                                  |
| raytrace                   | 250 ms                                                                 | 340 ms: 1.36x slower                                                   |
| richards_super             | 50.4 ms                                                                | 69.1 ms: 1.37x slower                                                  |
| richards                   | 44.4 ms                                                                | 60.9 ms: 1.37x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 67.5 ms: 1.37x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 519 ms: 1.38x slower                                                   |
| logging_simple             | 6.14 us                                                                | 8.58 us: 1.40x slower                                                  |
| logging_format             | 6.92 us                                                                | 9.75 us: 1.41x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.45x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 4.50 ms: 1.45x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 31.7 ms: 1.46x slower                                                  |
| mako                       | 11.2 ms                                                                | 16.7 ms: 1.49x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| generators                 | 28.5 ms                                                                | 44.3 ms: 1.55x slower                                                  |
| nbody                      | 85.3 ms                                                                | 139 ms: 1.63x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.20 ms: 3.46x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.7 ms: 8.97x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_iterparse, asyncio_websockets, pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.112x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.37x