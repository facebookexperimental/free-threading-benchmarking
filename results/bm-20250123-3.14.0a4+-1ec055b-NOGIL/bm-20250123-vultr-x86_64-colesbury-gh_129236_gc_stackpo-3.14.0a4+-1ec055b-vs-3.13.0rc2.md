# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_129236_gc_stackpo
- machine: linux-x86_64
- commit hash: 1ec055b
- commit date: 2025-01-23
- overall geometric mean: 1.078x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 303 ms: 1.17x slower                                                      |
| docutils       | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                    |
| html5lib       | 67.0 ms                                                      | 68.4 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                        | 1.09x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 578 ms: 1.58x faster                                                      |
| async_tree_io              | 876 ms                                                       | 611 ms: 1.43x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 321 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 507 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 538 ms: 1.24x faster                                                      |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                      |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                      |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                              |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                      |
| float          | 77.5 ms                                                      | 75.8 ms: 1.02x faster                                                     |
| nbody          | 85.1 ms                                                      | 132 ms: 1.56x slower                                                      |
| Geometric mean | (ref)                                                        | 1.10x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                     |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                              |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.2 ms: 1.09x faster                                                     |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                     |
| json_loads           | 27.0 us                                                      | 30.6 us: 1.13x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 69.3 ms: 1.17x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 246 us: 1.17x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.25x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 375 us: 1.27x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                     |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.8 ms: 1.23x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 27.4 ms: 1.27x slower                                                     |
| django_template | 34.1 ms                                                      | 44.0 ms: 1.29x slower                                                     |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.66 ms: 1.89x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 578 ms: 1.58x faster                                                      |
| async_tree_io              | 876 ms                                                       | 611 ms: 1.43x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 321 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 507 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 538 ms: 1.24x faster                                                      |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                      |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                      |
| deepcopy                   | 355 us                                                       | 316 us: 1.13x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.2 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.08 us: 1.06x faster                                                     |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                      |
| go                         | 141 ms                                                       | 137 ms: 1.03x faster                                                      |
| float                      | 77.5 ms                                                      | 75.8 ms: 1.02x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 38.4 us: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 18.9 ms: 1.01x faster                                                     |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                      |
| scimark_sor                | 134 ms                                                       | 136 ms: 1.01x slower                                                      |
| html5lib                   | 67.0 ms                                                      | 68.4 ms: 1.02x slower                                                     |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 3.19 us: 1.03x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.40 ms: 1.05x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.72 sec: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.44 ms: 1.08x slower                                                     |
| docutils                   | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                    |
| generators                 | 28.8 ms                                                      | 31.4 ms: 1.09x slower                                                     |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                     |
| scimark_fft                | 349 ms                                                       | 383 ms: 1.10x slower                                                      |
| mdp                        | 2.36 sec                                                     | 2.59 sec: 1.10x slower                                                    |
| pyflate                    | 449 ms                                                       | 495 ms: 1.10x slower                                                      |
| dulwich_log                | 74.8 ms                                                      | 82.5 ms: 1.10x slower                                                     |
| logging_silent             | 103 ns                                                       | 113 ns: 1.10x slower                                                      |
| pprint_safe_repr           | 738 ms                                                       | 826 ms: 1.12x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                     |
| json_loads                 | 27.0 us                                                      | 30.6 us: 1.13x slower                                                     |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                      |
| 2to3                       | 260 ms                                                       | 303 ms: 1.17x slower                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.49 ms: 1.17x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 69.3 ms: 1.17x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                    |
| thrift                     | 778 us                                                       | 909 us: 1.17x slower                                                      |
| unpickle_pure_python       | 210 us                                                       | 246 us: 1.17x slower                                                      |
| sqlglot_optimize           | 52.7 ms                                                      | 61.8 ms: 1.17x slower                                                     |
| coverage                   | 83.0 ms                                                      | 97.7 ms: 1.18x slower                                                     |
| logging_simple             | 6.16 us                                                      | 7.27 us: 1.18x slower                                                     |
| sympy_expand               | 457 ms                                                       | 548 ms: 1.20x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 187 ms: 1.20x slower                                                      |
| chaos                      | 57.3 ms                                                      | 69.7 ms: 1.22x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 7.30 ms: 1.22x slower                                                     |
| sympy_str                  | 275 ms                                                       | 335 ms: 1.22x slower                                                      |
| richards                   | 45.2 ms                                                      | 55.2 ms: 1.22x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 24.3 ms: 1.22x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.23x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 96.3 ms: 1.23x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 59.8 ms: 1.23x slower                                                     |
| logging_format             | 6.84 us                                                      | 8.41 us: 1.23x slower                                                     |
| richards_super             | 51.6 ms                                                      | 63.8 ms: 1.23x slower                                                     |
| scimark_lu                 | 113 ms                                                       | 139 ms: 1.24x slower                                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.0 ms: 1.24x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.25x slower                                                     |
| comprehensions             | 16.5 us                                                      | 20.6 us: 1.25x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 1.59 ms: 1.27x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 27.4 ms: 1.27x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 375 us: 1.27x slower                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 87.1 ms: 1.28x slower                                                     |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                      |
| django_template            | 34.1 ms                                                      | 44.0 ms: 1.29x slower                                                     |
| raytrace                   | 253 ms                                                       | 327 ms: 1.30x slower                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                     |
| fannkuch                   | 370 ms                                                       | 480 ms: 1.30x slower                                                      |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.31x slower                                                      |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                     |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 4.63 ms: 1.48x slower                                                     |
| nbody                      | 85.1 ms                                                      | 132 ms: 1.56x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                      | 95.0 ms: 8.64x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                              |

Benchmark hidden because not significant (3): regex_dna, coroutines, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250123-3.14.0a4+-1ec055b-NOGIL/bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x