# Results vs. 3.12.6

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.084x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 606 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                  |
| async_generators           | 384 ms                                                 | 358 ms: 1.07x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.8 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 90.7 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| regex_dna      | 168 ms                                                 | 167 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.8 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 26.4 us: 1.01x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.6 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 319 us: 1.04x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.6 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 606 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                   |
| deepcopy                   | 352 us                                                 | 255 us: 1.38x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.33x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                  |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                  |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 66.4 ms: 1.15x faster                                                  |
| raytrace                   | 299 ms                                                 | 261 ms: 1.15x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.14x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                  |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| spectral_norm              | 110 ms                                                 | 98.7 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.27 sec: 1.11x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.14 ms: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.10 us: 1.09x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 732 us: 1.08x faster                                                   |
| chaos                      | 62.8 ms                                                | 58.2 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| async_generators           | 384 ms                                                 | 358 ms: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                   |
| logging_format             | 7.35 us                                                | 6.88 us: 1.07x faster                                                  |
| scimark_fft                | 342 ms                                                 | 320 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.8 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.3 ms: 1.06x faster                                                  |
| pyflate                    | 448 ms                                                 | 422 ms: 1.06x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.06x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                 |
| float                      | 80.8 ms                                                | 76.8 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.59 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 711 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                 |
| json                       | 5.02 ms                                                | 4.82 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.3 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                   |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.94 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 76.3 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.03x faster                                                   |
| richards                   | 45.9 ms                                                | 44.7 ms: 1.03x faster                                                  |
| richards_super             | 51.9 ms                                                | 50.7 ms: 1.02x faster                                                  |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 459 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 52.3 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                  |
| json_loads                 | 26.5 us                                                | 26.4 us: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.6 ms: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 167 ms: 1.01x faster                                                   |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 50.6 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| nbody                      | 89.3 ms                                                | 90.7 ms: 1.02x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.46 sec: 1.02x slower                                                 |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.54 ms: 1.03x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 319 us: 1.04x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| telco                      | 6.53 ms                                                | 7.15 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.8 ms: 1.10x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.16 ms: 1.20x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.3 ms: 8.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): nqueens, fannkuch
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x