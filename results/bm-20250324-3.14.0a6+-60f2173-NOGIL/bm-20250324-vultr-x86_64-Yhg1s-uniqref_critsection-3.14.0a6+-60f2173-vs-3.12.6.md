# Results vs. 3.12.6

- fork: Yhg1s
- ref: uniqref_critsection
- machine: linux-x86_64
- commit hash: 60f2173
- commit date: 2025-03-24
- overall geometric mean: 1.041x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                                 |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                               |
| html5lib       | 63.6 ms                                                | 70.4 ms: 1.11x slower                                                |
| Geometric mean | (ref)                                                  | 1.10x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 555 ms: 2.00x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                 |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 537 ms: 1.35x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 572 ms: 1.25x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.4 ms: 1.06x faster                                                |
| pidigits       | 184 ms                                                 | 223 ms: 1.21x slower                                                 |
| nbody          | 89.3 ms                                                | 131 ms: 1.46x slower                                                 |
| Geometric mean | (ref)                                                  | 1.19x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                |
| regex_v8       | 20.6 ms                                                | 20.7 ms: 1.00x slower                                                |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                 |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.09x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                                |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 358 us: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.6 ms: 1.18x slower                                                |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.7 ms: 1.17x slower                                                |
| genshi_text     | 22.8 ms                                                | 28.2 ms: 1.23x slower                                                |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 555 ms: 2.00x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.81 ms: 1.91x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                 |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 537 ms: 1.35x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 572 ms: 1.25x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                |
| deepcopy                   | 352 us                                                 | 313 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                |
| dulwich_log                | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                |
| pathlib                    | 21.5 ms                                                | 20.0 ms: 1.08x faster                                                |
| float                      | 80.8 ms                                                | 76.4 ms: 1.06x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 39.2 us: 1.03x faster                                                |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 20.7 ms: 1.00x slower                                                |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                               |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                 |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.13 ms: 1.02x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.85 sec: 1.02x slower                                               |
| comprehensions             | 19.8 us                                                | 20.3 us: 1.02x slower                                                |
| generators                 | 32.2 ms                                                | 33.3 ms: 1.03x slower                                                |
| logging_silent             | 109 ns                                                 | 113 ns: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                               |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.3 ms: 1.07x slower                                                |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                 |
| raytrace                   | 299 ms                                                 | 320 ms: 1.07x slower                                                 |
| chaos                      | 62.8 ms                                                | 67.4 ms: 1.07x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.09x slower                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.35 us: 1.09x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                 |
| pyflate                    | 448 ms                                                 | 491 ms: 1.10x slower                                                 |
| thrift                     | 791 us                                                 | 872 us: 1.10x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.32 us: 1.10x slower                                                |
| html5lib                   | 63.6 ms                                                | 70.4 ms: 1.11x slower                                                |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.85 ms: 1.12x slower                                                |
| mdp                        | 2.42 sec                                               | 2.70 sec: 1.12x slower                                               |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                |
| json_loads                 | 26.5 us                                                | 29.8 us: 1.12x slower                                                |
| logging_format             | 7.35 us                                                | 8.27 us: 1.13x slower                                                |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 842 ms: 1.13x slower                                                 |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.14x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                               |
| sympy_str                  | 292 ms                                                 | 332 ms: 1.14x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.5 ms: 1.14x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 88.1 ms: 1.15x slower                                                |
| pickle_pure_python         | 308 us                                                 | 358 us: 1.16x slower                                                 |
| sympy_expand               | 468 ms                                                 | 547 ms: 1.17x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 58.7 ms: 1.17x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 69.6 ms: 1.18x slower                                                |
| richards                   | 45.9 ms                                                | 54.5 ms: 1.19x slower                                                |
| hexiom                     | 6.17 ms                                                | 7.37 ms: 1.19x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.20x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.3 ms: 1.20x slower                                                |
| pidigits                   | 184 ms                                                 | 223 ms: 1.21x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                                 |
| richards_super             | 51.9 ms                                                | 63.8 ms: 1.23x slower                                                |
| genshi_text                | 22.8 ms                                                | 28.2 ms: 1.23x slower                                                |
| nqueens                    | 80.1 ms                                                | 99.1 ms: 1.24x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                 |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.69 ms: 1.30x slower                                                |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 9.03 ms: 1.38x slower                                                |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                |
| nbody                      | 89.3 ms                                                | 131 ms: 1.46x slower                                                 |
| coverage                   | 71.4 ms                                                | 108 ms: 1.51x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 96.6 ms: 8.95x slower                                                |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                         |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250324-3.14.0a6+-60f2173-NOGIL/bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.041x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.38x