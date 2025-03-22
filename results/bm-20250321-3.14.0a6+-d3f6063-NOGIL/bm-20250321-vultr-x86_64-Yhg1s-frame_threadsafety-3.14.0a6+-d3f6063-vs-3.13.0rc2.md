# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: frame_threadsafety
- machine: linux-x86_64
- commit hash: d3f6063
- commit date: 2025-03-21
- overall geometric mean: 1.077x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.14x slower                                                |
| docutils       | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                              |
| html5lib       | 68.6 ms                                                                | 71.2 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 332 ms: 1.39x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 535 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 568 ms: 1.17x faster                                                |
| async_generators           | 375 ms                                                                 | 383 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                        |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 216 ms: 1.00x faster                                                |
| float          | 76.7 ms                                                                | 78.1 ms: 1.02x slower                                               |
| nbody          | 85.3 ms                                                                | 137 ms: 1.60x slower                                                |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                               |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.10x faster                                                |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                               |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.20x slower                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.0 ms: 1.07x faster                                               |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                |
| json_loads           | 27.3 us                                                                | 29.6 us: 1.08x slower                                               |
| xml_etree_generate   | 85.4 ms                                                                | 97.2 ms: 1.14x slower                                               |
| tomli_loads          | 2.01 sec                                                               | 2.34 sec: 1.16x slower                                              |
| xml_etree_process    | 59.2 ms                                                                | 70.5 ms: 1.19x slower                                               |
| unpickle_pure_python | 208 us                                                                 | 254 us: 1.22x slower                                                |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                               |
| pickle_pure_python   | 292 us                                                                 | 360 us: 1.23x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                               |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.6 ms: 1.21x slower                                               |
| django_template | 34.2 ms                                                                | 42.7 ms: 1.25x slower                                               |
| genshi_text     | 21.7 ms                                                                | 28.6 ms: 1.31x slower                                               |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.85x faster                                               |
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 332 ms: 1.39x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 535 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 568 ms: 1.17x faster                                                |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                |
| sqlite_synth               | 2.25 us                                                                | 1.99 us: 1.13x faster                                               |
| regex_effbot               | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                               |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.10x faster                                                |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                               |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.0 ms: 1.07x faster                                               |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 72.8 ms: 1.02x faster                                               |
| pidigits                   | 216 ms                                                                 | 216 ms: 1.00x faster                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                               |
| deepcopy_reduce            | 3.12 us                                                                | 3.17 us: 1.02x slower                                               |
| float                      | 76.7 ms                                                                | 78.1 ms: 1.02x slower                                               |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                               |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                               |
| scimark_sor                | 134 ms                                                                 | 137 ms: 1.02x slower                                                |
| async_generators           | 375 ms                                                                 | 383 ms: 1.02x slower                                                |
| deepcopy_memo              | 38.1 us                                                                | 39.2 us: 1.03x slower                                               |
| html5lib                   | 68.6 ms                                                                | 71.2 ms: 1.04x slower                                               |
| go                         | 141 ms                                                                 | 146 ms: 1.04x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                              |
| spectral_norm              | 108 ms                                                                 | 113 ms: 1.05x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                              |
| json_loads                 | 27.3 us                                                                | 29.6 us: 1.08x slower                                               |
| bpe_tokeniser              | 4.46 sec                                                               | 4.86 sec: 1.09x slower                                              |
| generators                 | 28.5 ms                                                                | 31.5 ms: 1.10x slower                                               |
| thrift                     | 772 us                                                                 | 855 us: 1.11x slower                                                |
| pyflate                    | 449 ms                                                                 | 499 ms: 1.11x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 97.2 ms: 1.14x slower                                               |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.14x slower                                                |
| scimark_fft                | 348 ms                                                                 | 400 ms: 1.15x slower                                                |
| logging_silent             | 98.2 ns                                                                | 114 ns: 1.16x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.34 sec: 1.16x slower                                              |
| telco                      | 7.77 ms                                                                | 9.06 ms: 1.17x slower                                               |
| pprint_safe_repr           | 719 ms                                                                 | 843 ms: 1.17x slower                                                |
| coverage                   | 82.5 ms                                                                | 97.6 ms: 1.18x slower                                               |
| mdp                        | 2.34 sec                                                               | 2.78 sec: 1.19x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.29 us: 1.19x slower                                               |
| logging_format             | 6.92 us                                                                | 8.21 us: 1.19x slower                                               |
| sympy_integrate            | 19.7 ms                                                                | 23.5 ms: 1.19x slower                                               |
| xml_etree_process          | 59.2 ms                                                                | 70.5 ms: 1.19x slower                                               |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.20x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.71 ms: 1.20x slower                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.75 sec: 1.20x slower                                              |
| sympy_expand               | 454 ms                                                                 | 549 ms: 1.21x slower                                                |
| genshi_xml                 | 49.1 ms                                                                | 59.6 ms: 1.21x slower                                               |
| unpickle_pure_python       | 208 us                                                                 | 254 us: 1.22x slower                                                |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                               |
| pickle_pure_python         | 292 us                                                                 | 360 us: 1.23x slower                                                |
| chaos                      | 56.3 ms                                                                | 69.4 ms: 1.23x slower                                               |
| richards                   | 44.4 ms                                                                | 55.2 ms: 1.24x slower                                               |
| deltablue                  | 3.10 ms                                                                | 3.86 ms: 1.25x slower                                               |
| django_template            | 34.2 ms                                                                | 42.7 ms: 1.25x slower                                               |
| comprehensions             | 16.6 us                                                                | 20.8 us: 1.25x slower                                               |
| nqueens                    | 77.7 ms                                                                | 97.8 ms: 1.26x slower                                               |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                                |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.2 ms: 1.26x slower                                               |
| richards_super             | 50.4 ms                                                                | 64.0 ms: 1.27x slower                                               |
| scimark_lu                 | 112 ms                                                                 | 144 ms: 1.28x slower                                                |
| hexiom                     | 5.95 ms                                                                | 7.69 ms: 1.29x slower                                               |
| raytrace                   | 250 ms                                                                 | 326 ms: 1.30x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 89.0 ms: 1.30x slower                                               |
| meteor_contest             | 101 ms                                                                 | 133 ms: 1.31x slower                                                |
| genshi_text                | 21.7 ms                                                                | 28.6 ms: 1.31x slower                                               |
| fannkuch                   | 376 ms                                                                 | 500 ms: 1.33x slower                                                |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                               |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                               |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                               |
| nbody                      | 85.3 ms                                                                | 137 ms: 1.60x slower                                                |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                               |
| bench_mp_pool              | 11.0 ms                                                                | 96.4 ms: 8.76x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                        |

Benchmark hidden because not significant (3): pylint, coroutines, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250321-3.14.0a6+-d3f6063-NOGIL/bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.37x