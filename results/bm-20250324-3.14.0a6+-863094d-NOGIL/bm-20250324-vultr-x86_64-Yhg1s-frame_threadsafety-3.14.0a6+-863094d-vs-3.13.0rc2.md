# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: frame_threadsafety
- machine: linux-x86_64
- commit hash: 863094d
- commit date: 2025-03-24
- overall geometric mean: 1.080x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 299 ms: 1.15x slower                                                |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                              |
| html5lib       | 68.6 ms                                                                | 71.5 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                                |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 333 ms: 1.38x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 551 ms: 1.15x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 586 ms: 1.14x faster                                                |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                               |
| async_generators           | 375 ms                                                                 | 382 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                               |
| pidigits       | 216 ms                                                                 | 220 ms: 1.02x slower                                                |
| nbody          | 85.3 ms                                                                | 138 ms: 1.62x slower                                                |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                               |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                               |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.20x slower                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 89.8 ms: 1.05x faster                                               |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                |
| json_loads           | 27.3 us                                                                | 29.2 us: 1.07x slower                                               |
| xml_etree_generate   | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                               |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.18x slower                                              |
| xml_etree_process    | 59.2 ms                                                                | 71.2 ms: 1.20x slower                                               |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                               |
| unpickle_pure_python | 208 us                                                                 | 258 us: 1.24x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.24x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                               |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.7 ms: 1.22x slower                                               |
| django_template | 34.2 ms                                                                | 42.8 ms: 1.25x slower                                               |
| genshi_text     | 21.7 ms                                                                | 28.4 ms: 1.31x slower                                               |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                               |
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                                |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 333 ms: 1.38x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 551 ms: 1.15x faster                                                |
| deepcopy                   | 357 us                                                                 | 312 us: 1.15x faster                                                |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 586 ms: 1.14x faster                                                |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                               |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                               |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.8 ms: 1.05x faster                                               |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 72.9 ms: 1.02x faster                                               |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                               |
| create_gc_cycles           | 1.33 ms                                                                | 1.34 ms: 1.01x slower                                               |
| float                      | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                               |
| deepcopy_reduce            | 3.12 us                                                                | 3.16 us: 1.01x slower                                               |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.02x slower                                                |
| pidigits                   | 216 ms                                                                 | 220 ms: 1.02x slower                                                |
| async_generators           | 375 ms                                                                 | 382 ms: 1.02x slower                                                |
| json                       | 4.98 ms                                                                | 5.09 ms: 1.02x slower                                               |
| deepcopy_memo              | 38.1 us                                                                | 39.0 us: 1.02x slower                                               |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                               |
| go                         | 141 ms                                                                 | 145 ms: 1.03x slower                                                |
| html5lib                   | 68.6 ms                                                                | 71.5 ms: 1.04x slower                                               |
| spectral_norm              | 108 ms                                                                 | 113 ms: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                              |
| json_loads                 | 27.3 us                                                                | 29.2 us: 1.07x slower                                               |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                              |
| bpe_tokeniser              | 4.46 sec                                                               | 4.87 sec: 1.09x slower                                              |
| thrift                     | 772 us                                                                 | 871 us: 1.13x slower                                                |
| generators                 | 28.5 ms                                                                | 32.2 ms: 1.13x slower                                               |
| pyflate                    | 449 ms                                                                 | 513 ms: 1.14x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                               |
| scimark_fft                | 348 ms                                                                 | 400 ms: 1.15x slower                                                |
| 2to3                       | 259 ms                                                                 | 299 ms: 1.15x slower                                                |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                              |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                |
| logging_simple             | 6.14 us                                                                | 7.18 us: 1.17x slower                                               |
| logging_format             | 6.92 us                                                                | 8.09 us: 1.17x slower                                               |
| telco                      | 7.77 ms                                                                | 9.09 ms: 1.17x slower                                               |
| pprint_safe_repr           | 719 ms                                                                 | 843 ms: 1.17x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.18x slower                                              |
| coverage                   | 82.5 ms                                                                | 98.1 ms: 1.19x slower                                               |
| sympy_integrate            | 19.7 ms                                                                | 23.5 ms: 1.19x slower                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.74 sec: 1.20x slower                                              |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.20x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                |
| xml_etree_process          | 59.2 ms                                                                | 71.2 ms: 1.20x slower                                               |
| sympy_str                  | 274 ms                                                                 | 333 ms: 1.21x slower                                                |
| genshi_xml                 | 49.1 ms                                                                | 59.7 ms: 1.22x slower                                               |
| sympy_expand               | 454 ms                                                                 | 555 ms: 1.22x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                               |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.83 ms: 1.23x slower                                               |
| chaos                      | 56.3 ms                                                                | 69.5 ms: 1.23x slower                                               |
| unpickle_pure_python       | 208 us                                                                 | 258 us: 1.24x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.24x slower                                                |
| django_template            | 34.2 ms                                                                | 42.8 ms: 1.25x slower                                               |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                                |
| richards                   | 44.4 ms                                                                | 56.1 ms: 1.26x slower                                               |
| comprehensions             | 16.6 us                                                                | 21.0 us: 1.27x slower                                               |
| nqueens                    | 77.7 ms                                                                | 98.6 ms: 1.27x slower                                               |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.94 ms: 1.27x slower                                               |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                |
| hexiom                     | 5.95 ms                                                                | 7.67 ms: 1.29x slower                                               |
| richards_super             | 50.4 ms                                                                | 65.0 ms: 1.29x slower                                               |
| scimark_monte_carlo        | 65.8 ms                                                                | 85.3 ms: 1.30x slower                                               |
| crypto_pyaes               | 68.2 ms                                                                | 88.5 ms: 1.30x slower                                               |
| genshi_text                | 21.7 ms                                                                | 28.4 ms: 1.31x slower                                               |
| raytrace                   | 250 ms                                                                 | 329 ms: 1.31x slower                                                |
| fannkuch                   | 376 ms                                                                 | 500 ms: 1.33x slower                                                |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                               |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                               |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                               |
| nbody                      | 85.3 ms                                                                | 138 ms: 1.62x slower                                                |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.41x slower                                               |
| bench_mp_pool              | 11.0 ms                                                                | 96.6 ms: 8.78x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                        |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250324-3.14.0a6+-863094d-NOGIL/bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.37x