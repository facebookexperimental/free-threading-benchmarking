# Results vs. 3.12.6

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.024x slower
- HPT reliability: 99.46%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 295 ms: 1.12x slower                                                   |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 69.1 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 561 ms: 1.98x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 592 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.5 ms: 1.08x faster                                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| regex_compile  | 142 ms                                                 | 145 ms: 1.02x slower                                                   |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.3 ms: 1.12x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.26 sec: 1.07x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 94.2 ms: 1.11x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 67.1 ms: 1.14x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 357 us: 1.16x slower                                                   |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                  |
| django_template | 34.7 ms                                                | 40.9 ms: 1.18x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.1 ms: 1.19x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 2.00x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 561 ms: 1.98x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 592 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                  |
| deepcopy                   | 352 us                                                 | 299 us: 1.18x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 86.3 ms: 1.12x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 37.0 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| float                      | 80.8 ms                                                | 74.5 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| go                         | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| spectral_norm              | 110 ms                                                 | 104 ms: 1.06x faster                                                   |
| generators                 | 32.2 ms                                                | 30.4 ms: 1.06x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.57 sec: 1.04x faster                                                 |
| comprehensions             | 19.8 us                                                | 19.1 us: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                   |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                   |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.01x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.11 us: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 145 ms: 1.02x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 80.8 ms: 1.03x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                 |
| raytrace                   | 299 ms                                                 | 313 ms: 1.05x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 779 ms: 1.05x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.54 sec: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                                  |
| chaos                      | 62.8 ms                                                | 67.0 ms: 1.07x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.26 sec: 1.07x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                   |
| pyflate                    | 448 ms                                                 | 483 ms: 1.08x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.18 us: 1.08x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                  |
| html5lib                   | 63.6 ms                                                | 69.1 ms: 1.09x slower                                                  |
| logging_format             | 7.35 us                                                | 8.00 us: 1.09x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.09x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 117 ms: 1.09x slower                                                   |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| scimark_fft                | 342 ms                                                 | 376 ms: 1.10x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 94.2 ms: 1.11x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.85 ms: 1.11x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 59.4 ms: 1.11x slower                                                  |
| 2to3                       | 264 ms                                                 | 295 ms: 1.12x slower                                                   |
| sympy_str                  | 292 ms                                                 | 329 ms: 1.13x slower                                                   |
| thrift                     | 791 us                                                 | 896 us: 1.13x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.54 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 67.1 ms: 1.14x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.1 ms: 1.14x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.5 ms: 1.14x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                   |
| hexiom                     | 6.17 ms                                                | 7.08 ms: 1.15x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| sympy_expand               | 468 ms                                                 | 539 ms: 1.15x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 357 us: 1.16x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 79.9 ms: 1.17x slower                                                  |
| nqueens                    | 80.1 ms                                                | 93.8 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                  |
| richards                   | 45.9 ms                                                | 54.0 ms: 1.18x slower                                                  |
| django_template            | 34.7 ms                                                | 40.9 ms: 1.18x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.1 ms: 1.19x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                   |
| richards_super             | 51.9 ms                                                | 62.5 ms: 1.21x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.49 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.25x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.43 ms: 1.29x slower                                                  |
| fannkuch                   | 372 ms                                                 | 482 ms: 1.29x slower                                                   |
| telco                      | 6.53 ms                                                | 8.46 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 96.5 ms: 1.35x slower                                                  |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 90.4 ms: 8.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 99.46% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x