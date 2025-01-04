# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: 33deca3
- commit date: 2025-01-03
- overall geometric mean: 1.059x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 312 ms: 1.19x slower                                                 |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                               |
| html5lib       | 63.6 ms                                                | 72.9 ms: 1.15x slower                                                |
| Geometric mean | (ref)                                                  | 1.13x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.90x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.81x faster                                                 |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                 |
| async_generators           | 384 ms                                                 | 419 ms: 1.09x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.1 ms: 1.02x faster                                                |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                 |
| nbody          | 89.3 ms                                                | 132 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                 |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.15x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                 |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                               |
| unpickle_pure_python | 221 us                                                 | 249 us: 1.13x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                |
| pickle_pure_python   | 308 us                                                 | 373 us: 1.21x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.71 ms: 1.36x slower                                                |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 61.2 ms: 1.22x slower                                                |
| genshi_text     | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                |
| django_template | 34.7 ms                                                | 43.5 ms: 1.25x slower                                                |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.90x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.81x faster                                                 |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                |
| deepcopy                   | 352 us                                                 | 318 us: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                                |
| json                       | 5.02 ms                                                | 4.84 ms: 1.04x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                |
| float                      | 80.8 ms                                                | 79.1 ms: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.76 sec: 1.00x slower                                               |
| go                         | 139 ms                                                 | 140 ms: 1.00x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.21 sec: 1.03x slower                                               |
| dulwich_log                | 78.9 ms                                                | 81.8 ms: 1.04x slower                                                |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                                |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                 |
| scimark_sor                | 130 ms                                                 | 136 ms: 1.05x slower                                                 |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                                 |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                                |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                 |
| logging_silent             | 109 ns                                                 | 117 ns: 1.07x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.07x slower                                               |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.34 us: 1.08x slower                                                |
| pyflate                    | 448 ms                                                 | 488 ms: 1.09x slower                                                 |
| async_generators           | 384 ms                                                 | 419 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 819 ms: 1.10x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                               |
| raytrace                   | 299 ms                                                 | 331 ms: 1.11x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.35 us: 1.11x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                               |
| scimark_fft                | 342 ms                                                 | 382 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 249 us: 1.13x slower                                                 |
| logging_format             | 7.35 us                                                | 8.29 us: 1.13x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 86.7 ms: 1.13x slower                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.7 ms: 1.13x slower                                                |
| chaos                      | 62.8 ms                                                | 71.3 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                 |
| html5lib                   | 63.6 ms                                                | 72.9 ms: 1.15x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                                 |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.15x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.94 ms: 1.16x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                |
| thrift                     | 791 us                                                 | 926 us: 1.17x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 62.5 ms: 1.17x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.18x slower                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                |
| sympy_expand               | 468 ms                                                 | 554 ms: 1.18x slower                                                 |
| 2to3                       | 264 ms                                                 | 312 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.3 ms: 1.20x slower                                                |
| pickle_pure_python         | 308 us                                                 | 373 us: 1.21x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.51 ms: 1.22x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 61.2 ms: 1.22x slower                                                |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                                |
| richards                   | 45.9 ms                                                | 56.0 ms: 1.22x slower                                                |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                                 |
| genshi_text                | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                |
| django_template            | 34.7 ms                                                | 43.5 ms: 1.25x slower                                                |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                |
| richards_super             | 51.9 ms                                                | 65.4 ms: 1.26x slower                                                |
| fannkuch                   | 372 ms                                                 | 480 ms: 1.29x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                                |
| telco                      | 6.53 ms                                                | 8.73 ms: 1.34x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 9.71 ms: 1.36x slower                                                |
| coverage                   | 71.4 ms                                                | 98.8 ms: 1.38x slower                                                |
| deltablue                  | 3.45 ms                                                | 4.80 ms: 1.39x slower                                                |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                |
| nbody                      | 89.3 ms                                                | 132 ms: 1.47x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.54x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 97.8 ms: 9.06x slower                                                |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                         |

Benchmark hidden because not significant (2): spectral_norm, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250103-3.14.0a3+-33deca3-NOGIL/bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x