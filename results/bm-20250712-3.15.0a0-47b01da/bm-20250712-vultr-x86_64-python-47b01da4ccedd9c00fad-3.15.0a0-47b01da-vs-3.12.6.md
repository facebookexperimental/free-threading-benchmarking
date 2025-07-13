# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.069x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| html5lib       | 63.6 ms                                                | 61.7 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 617 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                                  |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 497 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.4 ms: 1.13x faster                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.09x faster                                                |
| unpickle_pure_python | 221 us                                                 | 206 us: 1.07x faster                                                  |
| pickle_dict          | 31.8 us                                                | 30.5 us: 1.04x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 93.1 ms: 1.04x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.1 ms: 1.02x faster                                                 |
| unpickle             | 14.1 us                                                | 13.8 us: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| unpickle_list        | 4.67 us                                                | 4.96 us: 1.06x slower                                                 |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.09 us: 1.07x slower                                                 |
| pickle               | 10.9 us                                                | 12.2 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 617 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                                  |
| deepcopy                   | 352 us                                                 | 250 us: 1.41x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.6 us: 1.41x faster                                                 |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 42.1 ns: 1.24x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.20x faster                                                  |
| raytrace                   | 299 ms                                                 | 250 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.82 us: 1.14x faster                                                 |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                  |
| float                      | 80.8 ms                                                | 71.4 ms: 1.13x faster                                                 |
| logging_silent             | 109 ns                                                 | 96.3 ns: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                |
| logging_format             | 7.35 us                                                | 6.51 us: 1.13x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.08 ms: 1.12x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.2 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.1 ms: 1.12x faster                                                 |
| pyflate                    | 448 ms                                                 | 400 ms: 1.12x faster                                                  |
| spectral_norm              | 110 ms                                                 | 99.3 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.8 ms: 1.11x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.59 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.09x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 62.5 ms: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 206 us: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 703 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 752 us: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.5 ms: 1.05x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 497 ms: 1.04x faster                                                  |
| pickle_dict                | 31.8 us                                                | 30.5 us: 1.04x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.1 ms: 1.04x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.7 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.1 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.5 ms: 1.02x faster                                                 |
| scimark_fft                | 342 ms                                                 | 336 ms: 1.02x faster                                                  |
| unpickle                   | 14.1 us                                                | 13.8 us: 1.02x faster                                                 |
| django_template            | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.04x slower                                                 |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.66 ms: 1.06x slower                                                 |
| unpickle_list              | 4.67 us                                                | 4.96 us: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.09 us: 1.07x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| pickle                     | 10.9 us                                                | 12.2 us: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 80.8 ms: 1.13x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.69 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.79x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.51x slower                                                  |
| telco                      | 6.53 ms                                                | 159 ms: 24.42x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): nbody, asyncio_websockets
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x