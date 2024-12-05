# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.223x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 366 ms: 1.39x slower                                                  |
| docutils       | 2.64 sec                                               | 3.10 sec: 1.18x slower                                                |
| html5lib       | 63.6 ms                                                | 99.4 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                  | 1.37x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 819 ms: 1.36x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 850 ms: 1.27x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 355 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 447 ms: 1.25x faster                                                  |
| async_tree_none            | 464 ms                                                 | 388 ms: 1.20x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 471 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 617 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 645 ms: 1.11x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                 |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| nbody          | 89.3 ms                                                | 128 ms: 1.43x slower                                                  |
| float          | 80.8 ms                                                | 138 ms: 1.71x slower                                                  |
| Geometric mean | (ref)                                                  | 1.34x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                 |
| regex_compile  | 142 ms                                                 | 179 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.2 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 29.0 us: 1.09x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.68 sec: 1.27x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 77.3 ms: 1.31x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 331 us: 1.50x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 508 us: 1.65x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.77x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.9 ms: 1.25x slower                                                 |
| genshi_text     | 22.8 ms                                                | 31.4 ms: 1.37x slower                                                 |
| django_template | 34.7 ms                                                | 50.8 ms: 1.46x slower                                                 |
| mako            | 11.0 ms                                                | 17.6 ms: 1.60x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 819 ms: 1.36x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 850 ms: 1.27x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 355 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 447 ms: 1.25x faster                                                  |
| async_tree_none            | 464 ms                                                 | 388 ms: 1.20x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 471 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 617 ms: 1.17x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 645 ms: 1.11x faster                                                  |
| deepcopy                   | 352 us                                                 | 327 us: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.2 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.2 ms: 1.06x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.5 us: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.10 ms: 1.01x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.03x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.97 sec: 1.05x slower                                                |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.0 us: 1.09x slower                                                 |
| spectral_norm              | 110 ms                                                 | 124 ms: 1.12x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.50 us: 1.14x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.15x slower                                                |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                 |
| scimark_fft                | 342 ms                                                 | 401 ms: 1.18x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.10 sec: 1.18x slower                                                |
| generators                 | 32.2 ms                                                | 38.2 ms: 1.18x slower                                                 |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 91.9 ms: 1.20x slower                                                 |
| pylint                     | 319 ms                                                 | 383 ms: 1.20x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 95.8 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                  |
| nqueens                    | 80.1 ms                                                | 99.4 ms: 1.24x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 62.9 ms: 1.25x slower                                                 |
| regex_compile              | 142 ms                                                 | 179 ms: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.68 sec: 1.27x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 137 ms: 1.29x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 68.9 ms: 1.29x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 963 ms: 1.30x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 77.3 ms: 1.31x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 2.00 sec: 1.31x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.55 sec: 1.33x slower                                                |
| fannkuch                   | 372 ms                                                 | 496 ms: 1.33x slower                                                  |
| telco                      | 6.53 ms                                                | 8.75 ms: 1.34x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.95 ms: 1.36x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.7 ms: 1.36x slower                                                 |
| genshi_text                | 22.8 ms                                                | 31.4 ms: 1.37x slower                                                 |
| comprehensions             | 19.8 us                                                | 27.3 us: 1.38x slower                                                 |
| 2to3                       | 264 ms                                                 | 366 ms: 1.39x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 203 ms: 1.42x slower                                                  |
| nbody                      | 89.3 ms                                                | 128 ms: 1.43x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| coverage                   | 71.4 ms                                                | 104 ms: 1.45x slower                                                  |
| thrift                     | 791 us                                                 | 1.15 ms: 1.46x slower                                                 |
| django_template            | 34.7 ms                                                | 50.8 ms: 1.46x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 331 us: 1.50x slower                                                  |
| pyflate                    | 448 ms                                                 | 684 ms: 1.53x slower                                                  |
| html5lib                   | 63.6 ms                                                | 99.4 ms: 1.56x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 181 ms: 1.59x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.80 ms: 1.59x slower                                                 |
| mako                       | 11.0 ms                                                | 17.6 ms: 1.60x slower                                                 |
| chaos                      | 62.8 ms                                                | 103 ms: 1.64x slower                                                  |
| sympy_str                  | 292 ms                                                 | 477 ms: 1.64x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.64x slower                                                 |
| logging_silent             | 109 ns                                                 | 179 ns: 1.64x slower                                                  |
| richards_super             | 51.9 ms                                                | 85.5 ms: 1.65x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 508 us: 1.65x slower                                                  |
| logging_format             | 7.35 us                                                | 12.2 us: 1.65x slower                                                 |
| richards                   | 45.9 ms                                                | 76.1 ms: 1.66x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                 |
| float                      | 80.8 ms                                                | 138 ms: 1.71x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.73x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.94 ms: 1.76x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.77x slower                                                 |
| scimark_sor                | 130 ms                                                 | 233 ms: 1.80x slower                                                  |
| raytrace                   | 299 ms                                                 | 543 ms: 1.82x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.56 ms: 1.89x slower                                                 |
| go                         | 139 ms                                                 | 265 ms: 1.90x slower                                                  |
| sympy_expand               | 468 ms                                                 | 956 ms: 2.04x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 351 ms: 2.12x slower                                                  |
| deltablue                  | 3.45 ms                                                | 7.92 ms: 2.30x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.37 ms: 3.58x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.11x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241204-3.14.0a2+-c0d3c19-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.223x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x