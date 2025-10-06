# Results vs. 3.12.6

- fork: python
- ref: 3195da0b1a5dc8a03faa
- machine: linux-x86_64
- commit hash: 3195da0
- commit date: 2025-10-05
- overall geometric mean: 1.013x slower
- HPT reliability: 79.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                  |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| html5lib       | 63.6 ms                                                | 66.7 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 514 ms: 2.16x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 539 ms: 2.01x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 279 ms: 2.01x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 222 ms: 2.01x faster                                                  |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                 |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                                  |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.04 sec: 1.03x faster                                                |
| unpickle_pure_python | 221 us                                                 | 230 us: 1.05x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 340 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.3 ms: 1.15x slower                                                 |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 514 ms: 2.16x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 539 ms: 2.01x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 279 ms: 2.01x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 222 ms: 2.01x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.95 ms: 1.77x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.9 us: 1.30x faster                                                 |
| deepcopy                   | 352 us                                                 | 281 us: 1.25x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                                 |
| float                      | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| generators                 | 32.2 ms                                                | 30.2 ms: 1.07x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.98 us: 1.03x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 2.04 sec: 1.03x faster                                                |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                  |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| raytrace                   | 299 ms                                                 | 297 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.1 ms: 1.00x slower                                                 |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                                  |
| scimark_fft                | 342 ms                                                 | 344 ms: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.50 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.82 us: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 462 ms: 1.03x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 230 us: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.46 ms: 1.05x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.7 ms: 1.05x slower                                                 |
| logging_format             | 7.35 us                                                | 7.71 us: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 791 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                  |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                                |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| json                       | 5.02 ms                                                | 5.42 ms: 1.08x slower                                                 |
| richards                   | 45.9 ms                                                | 50.6 ms: 1.10x slower                                                 |
| nqueens                    | 80.1 ms                                                | 88.4 ms: 1.10x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 340 us: 1.10x slower                                                  |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 523 ms: 1.12x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                 |
| richards_super             | 51.9 ms                                                | 58.7 ms: 1.13x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.9 ms: 1.14x slower                                                 |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.3 ms: 1.15x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.16x slower                                                  |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.32 ms: 1.21x slower                                                 |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.52 ms: 1.39x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 15.2 ms: 1.40x slower                                                 |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                  |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.06 ms: 3.25x slower                                                 |
| telco                      | 6.53 ms                                                | 175 ms: 26.82x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (2): pycparser, regex_v8
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 79.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x