# Results vs. 3.12.6

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 327 ms: 1.70x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 653 ms: 1.70x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 638 ms: 1.70x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 266 ms: 1.67x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                   |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.2 ms: 1.10x faster                                                  |
| nbody          | 89.3 ms                                                | 94.6 ms: 1.06x slower                                                  |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                  |
| regex_compile  | 142 ms                                                 | 132 ms: 1.08x faster                                                   |
| regex_dna      | 168 ms                                                 | 179 ms: 1.06x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.05x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 94.4 ms: 1.02x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 223 us: 1.01x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 86.2 ms: 1.01x slower                                                  |
| json_loads           | 26.5 us                                                | 27.1 us: 1.02x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 320 us: 1.04x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 61.3 ms: 1.04x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.65 ms: 1.21x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.8 ms: 1.05x faster                                                  |
| django_template | 34.7 ms                                                | 36.6 ms: 1.06x slower                                                  |
| mako            | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.04x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 327 ms: 1.70x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 653 ms: 1.70x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 638 ms: 1.70x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 266 ms: 1.67x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                   |
| deepcopy                   | 352 us                                                 | 260 us: 1.35x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                  |
| go                         | 139 ms                                                 | 114 ms: 1.22x faster                                                   |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 68.7 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.14x faster                                                  |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.71 us: 1.13x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 56.0 ms: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                  |
| spectral_norm              | 110 ms                                                 | 99.1 ms: 1.11x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 288 ms: 1.11x faster                                                   |
| float                      | 80.8 ms                                                | 73.2 ms: 1.10x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 70.5 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                  |
| regex_compile              | 142 ms                                                 | 132 ms: 1.08x faster                                                   |
| pyflate                    | 448 ms                                                 | 417 ms: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 134 ms: 1.06x faster                                                   |
| scimark_fft                | 342 ms                                                 | 321 ms: 1.06x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.5 ms: 1.06x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.26 us: 1.06x faster                                                  |
| richards                   | 45.9 ms                                                | 43.7 ms: 1.05x faster                                                  |
| logging_format             | 7.35 us                                                | 7.01 us: 1.05x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.8 ms: 1.05x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.05x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.8 ms: 1.04x faster                                                  |
| generators                 | 32.2 ms                                                | 31.2 ms: 1.03x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                  |
| sympy_str                  | 292 ms                                                 | 283 ms: 1.03x faster                                                   |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.36 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.4 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 162 ms: 1.02x faster                                                   |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 161 us: 1.02x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 737 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.51 sec: 1.01x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 223 us: 1.01x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 86.2 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.46 ms: 1.01x slower                                                  |
| nqueens                    | 80.1 ms                                                | 81.8 ms: 1.02x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.1 us: 1.02x slower                                                  |
| sympy_expand               | 468 ms                                                 | 480 ms: 1.03x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 118 ms: 1.04x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 320 us: 1.04x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 61.3 ms: 1.04x slower                                                  |
| django_template            | 34.7 ms                                                | 36.6 ms: 1.06x slower                                                  |
| fannkuch                   | 372 ms                                                 | 394 ms: 1.06x slower                                                   |
| nbody                      | 89.3 ms                                                | 94.6 ms: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.06x slower                                                   |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| mako                       | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.4 ms: 1.11x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.06 ms: 1.13x slower                                                  |
| telco                      | 6.53 ms                                                | 7.41 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.65 ms: 1.21x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 90.1 ms: 8.35x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (5): asyncio_websockets, sqlite_synth, hexiom, genshi_xml, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x