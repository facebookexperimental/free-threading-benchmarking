# Results vs. 3.12.6

- fork: python
- ref: c90863ac3dcbc5b0b8f9
- machine: linux-x86_64
- commit hash: c90863a
- commit date: 2025-12-12
- overall geometric mean: 1.075x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.0 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 502 ms: 1.42x faster                                                   |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.5 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 86.7 ms: 1.03x faster                                                  |
| pidigits       | 184 ms                                                 | 215 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.2 ms: 1.15x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.90 ms: 1.05x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.7 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.00x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                 |
| json_loads           | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.9 ms: 1.03x faster                                                  |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.9 us: 1.50x faster                                                  |
| deepcopy                   | 352 us                                                 | 242 us: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 502 ms: 1.42x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                  |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                   |
| raytrace                   | 299 ms                                                 | 250 ms: 1.20x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.0 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.70 us: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.5 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.2 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| spectral_norm              | 110 ms                                                 | 96.5 ms: 1.14x faster                                                  |
| logging_format             | 7.35 us                                                | 6.44 us: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.16 sec: 1.14x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.2 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                   |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                   |
| generators                 | 32.2 ms                                                | 28.6 ms: 1.13x faster                                                  |
| scimark_fft                | 342 ms                                                 | 304 ms: 1.12x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 68.9 ms: 1.11x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.60 ms: 1.10x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| logging_silent             | 109 ns                                                 | 99.8 ns: 1.09x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 413 ms: 1.08x faster                                                   |
| richards                   | 45.9 ms                                                | 42.4 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.2 ms: 1.08x faster                                                  |
| 2to3                       | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| html5lib                   | 63.6 ms                                                | 59.0 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.4 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 698 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.90 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 767 us: 1.03x faster                                                   |
| nbody                      | 89.3 ms                                                | 86.7 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.28 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.9 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 57.7 ms: 1.02x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.38 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.8 ms: 1.02x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.00x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                 |
| sympy_expand               | 468 ms                                                 | 482 ms: 1.03x slower                                                   |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                   |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| fannkuch                   | 372 ms                                                 | 393 ms: 1.06x slower                                                   |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.00 ms: 1.16x slower                                                  |
| coverage                   | 71.4 ms                                                | 82.8 ms: 1.16x slower                                                  |
| pidigits                   | 184 ms                                                 | 215 ms: 1.17x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.17x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 282 ms: 26.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): coroutines, json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x