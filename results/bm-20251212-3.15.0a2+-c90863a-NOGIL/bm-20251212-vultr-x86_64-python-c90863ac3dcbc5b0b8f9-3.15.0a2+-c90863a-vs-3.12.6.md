# Results vs. 3.12.6

- fork: python
- ref: c90863ac3dcbc5b0b8f9
- machine: linux-x86_64
- commit hash: c90863a
- commit date: 2025-12-12
- overall geometric mean: 1.034x slower
- HPT reliability: 84.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| docutils       | 2.64 sec                                               | 2.76 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 67.4 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 628 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 328 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 521 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 547 ms: 1.31x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.0 ms: 1.12x faster                                                  |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                   |
| nbody          | 89.3 ms                                                | 122 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                  |
| regex_compile  | 142 ms                                                 | 142 ms: 1.00x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                  |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.08x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.09x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 98.8 ms: 1.16x slower                                                  |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.6 ms: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.70 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                  |
| genshi_xml      | 50.2 ms                                                | 58.9 ms: 1.17x slower                                                  |
| django_template | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                  |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 628 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 328 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.14 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 521 ms: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 547 ms: 1.31x faster                                                   |
| deepcopy                   | 352 us                                                 | 278 us: 1.27x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| float                      | 80.8 ms                                                | 72.0 ms: 1.12x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.09x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 72.1 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                   |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.06x faster                                                   |
| generators                 | 32.2 ms                                                | 30.8 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                 |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.98 us: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| regex_compile              | 142 ms                                                 | 142 ms: 1.00x faster                                                   |
| pyflate                    | 448 ms                                                 | 455 ms: 1.02x slower                                                   |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.44 ms: 1.04x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.76 sec: 1.04x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.96 us: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.65 ms: 1.06x slower                                                  |
| html5lib                   | 63.6 ms                                                | 67.4 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                   |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 795 ms: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                   |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                   |
| logging_format             | 7.35 us                                                | 7.91 us: 1.08x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.08x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| nqueens                    | 80.1 ms                                                | 86.6 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.08x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 85.5 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 529 ms: 1.13x slower                                                   |
| thrift                     | 791 us                                                 | 897 us: 1.13x slower                                                   |
| richards                   | 45.9 ms                                                | 52.1 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.9 ms: 1.14x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.14x slower                                                   |
| richards_super             | 51.9 ms                                                | 59.7 ms: 1.15x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.08 ms: 1.16x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 98.8 ms: 1.16x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                  |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 58.9 ms: 1.17x slower                                                  |
| django_template            | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 70.6 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                   |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.70 ms: 1.35x slower                                                  |
| nbody                      | 89.3 ms                                                | 122 ms: 1.36x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.38x slower                                                  |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 178 ms: 27.30x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): spectral_norm, chaos, scimark_fft
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x slower

# HPT report

- Reliability score: 84.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x