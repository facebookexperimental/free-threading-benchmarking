# Results vs. 3.12.6

- fork: nascheme
- ref: gh_132380_tp_lookup_
- machine: linux-x86_64
- commit hash: d3f79e5
- commit date: 2025-04-17
- overall geometric mean: 1.027x faster
- HPT reliability: 68.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.06x slower                                                     |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.01x slower                                                   |
| html5lib       | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 518 ms: 2.14x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 543 ms: 1.99x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.98x faster                                                     |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                     |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.0 ms: 1.21x faster                                                    |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                     |
| nbody          | 89.3 ms                                                | 110 ms: 1.23x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                    |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                    |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.08 sec: 1.01x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 225 us: 1.02x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 325 us: 1.06x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 93.0 ms: 1.09x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 66.4 ms: 1.13x slower                                                    |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                    |
| json_dumps           | 10.4 ms                                                | 12.6 ms: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.0 ms: 1.10x slower                                                    |
| genshi_text     | 22.8 ms                                                | 25.9 ms: 1.13x slower                                                    |
| django_template | 34.7 ms                                                | 39.7 ms: 1.14x slower                                                    |
| mako            | 11.0 ms                                                | 15.2 ms: 1.39x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 518 ms: 2.14x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 543 ms: 1.99x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.98x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.96x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                   |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                     |
| deepcopy                   | 352 us                                                 | 289 us: 1.22x faster                                                     |
| float                      | 80.8 ms                                                | 67.0 ms: 1.21x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 34.6 us: 1.17x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 70.2 ms: 1.12x faster                                                    |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                                     |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                    |
| scimark_sor                | 130 ms                                                 | 117 ms: 1.11x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                     |
| logging_silent             | 109 ns                                                 | 102 ns: 1.06x faster                                                     |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                     |
| spectral_norm              | 110 ms                                                 | 104 ms: 1.05x faster                                                     |
| generators                 | 32.2 ms                                                | 30.6 ms: 1.05x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.51 sec: 1.05x faster                                                   |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                   |
| comprehensions             | 19.8 us                                                | 19.1 us: 1.04x faster                                                    |
| raytrace                   | 299 ms                                                 | 289 ms: 1.04x faster                                                     |
| chaos                      | 62.8 ms                                                | 61.3 ms: 1.02x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 2.08 sec: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.01x slower                                                   |
| pyflate                    | 448 ms                                                 | 455 ms: 1.02x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 225 us: 1.02x slower                                                     |
| json                       | 5.02 ms                                                | 5.16 ms: 1.03x slower                                                    |
| scimark_fft                | 342 ms                                                 | 353 ms: 1.03x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 773 ms: 1.04x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.59 ms: 1.04x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.58 sec: 1.04x slower                                                   |
| html5lib                   | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                    |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                     |
| logging_simple             | 6.63 us                                                | 6.97 us: 1.05x slower                                                    |
| 2to3                       | 264 ms                                                 | 278 ms: 1.06x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 325 us: 1.06x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                    |
| logging_format             | 7.35 us                                                | 7.83 us: 1.07x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.4 ms: 1.07x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.63 ms: 1.07x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 73.7 ms: 1.08x slower                                                    |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 154 ms: 1.08x slower                                                     |
| nqueens                    | 80.1 ms                                                | 86.7 ms: 1.08x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 83.1 ms: 1.08x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 93.0 ms: 1.09x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 55.0 ms: 1.10x slower                                                    |
| richards                   | 45.9 ms                                                | 50.8 ms: 1.11x slower                                                    |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.94 ms: 1.12x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 66.4 ms: 1.13x slower                                                    |
| richards_super             | 51.9 ms                                                | 58.5 ms: 1.13x slower                                                    |
| genshi_text                | 22.8 ms                                                | 25.9 ms: 1.13x slower                                                    |
| sympy_expand               | 468 ms                                                 | 531 ms: 1.13x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                     |
| django_template            | 34.7 ms                                                | 39.7 ms: 1.14x slower                                                    |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                                     |
| fannkuch                   | 372 ms                                                 | 451 ms: 1.21x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 12.6 ms: 1.22x slower                                                    |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                    |
| nbody                      | 89.3 ms                                                | 110 ms: 1.23x slower                                                     |
| telco                      | 6.53 ms                                                | 8.27 ms: 1.27x slower                                                    |
| mako                       | 11.0 ms                                                | 15.2 ms: 1.39x slower                                                    |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.14 ms: 3.33x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 94.9 ms: 8.79x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): regex_compile, asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250417-3.14.0a7+-d3f79e5-NOGIL/bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 68.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x