# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 39cab3f
- commit date: 2024-12-12
- overall geometric mean: 1.136x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 342 ms: 1.30x slower                                                  |
| docutils       | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                |
| html5lib       | 63.6 ms                                                | 78.3 ms: 1.23x slower                                                 |
| Geometric mean | (ref)                                                  | 1.20x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 637 ms: 1.74x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 272 ms: 1.64x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 662 ms: 1.64x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 346 ms: 1.62x faster                                                  |
| async_tree_none            | 464 ms                                                 | 309 ms: 1.50x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 377 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 524 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 550 ms: 1.30x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| async_generators           | 384 ms                                                 | 423 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| float          | 80.8 ms                                                | 109 ms: 1.35x slower                                                  |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                  | 1.26x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| regex_compile  | 142 ms                                                 | 161 ms: 1.13x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 257 us: 1.17x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 370 us: 1.20x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.28x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 77.4 ms: 1.31x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 14.2 ms: 1.99x slower                                                 |
| python_startup         | 9.93 ms                                                | 23.6 ms: 2.38x slower                                                 |
| Geometric mean         | (ref)                                                  | 2.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 61.1 ms: 1.22x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                 |
| django_template | 34.7 ms                                                | 44.3 ms: 1.28x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 637 ms: 1.74x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 272 ms: 1.64x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 662 ms: 1.64x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 346 ms: 1.62x faster                                                  |
| async_tree_none            | 464 ms                                                 | 309 ms: 1.50x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 377 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 524 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 550 ms: 1.30x faster                                                  |
| deepcopy                   | 352 us                                                 | 315 us: 1.12x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.27 ms: 1.06x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.5 us: 1.05x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.13 us: 1.03x faster                                                 |
| generators                 | 32.2 ms                                                | 31.2 ms: 1.03x faster                                                 |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.81 sec: 1.01x slower                                                |
| logging_silent             | 109 ns                                                 | 112 ns: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                                 |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 85.8 ms: 1.09x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.36 us: 1.09x slower                                                 |
| async_generators           | 384 ms                                                 | 423 ms: 1.10x slower                                                  |
| spectral_norm              | 110 ms                                                 | 121 ms: 1.10x slower                                                  |
| pylint                     | 319 ms                                                 | 352 ms: 1.11x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                                 |
| regex_compile              | 142 ms                                                 | 161 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.34 sec: 1.14x slower                                                |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.15x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                                  |
| scimark_fft                | 342 ms                                                 | 397 ms: 1.16x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.17x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 257 us: 1.17x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 63.1 ms: 1.18x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 882 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.83 sec: 1.20x slower                                                |
| pickle_pure_python         | 308 us                                                 | 370 us: 1.20x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 61.1 ms: 1.22x slower                                                 |
| go                         | 139 ms                                                 | 170 ms: 1.22x slower                                                  |
| pyflate                    | 448 ms                                                 | 547 ms: 1.22x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                 |
| nqueens                    | 80.1 ms                                                | 98.1 ms: 1.22x slower                                                 |
| html5lib                   | 63.6 ms                                                | 78.3 ms: 1.23x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                |
| logging_simple             | 6.63 us                                                | 8.23 us: 1.24x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 178 ms: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.84 ms: 1.27x slower                                                 |
| raytrace                   | 299 ms                                                 | 381 ms: 1.27x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.28x slower                                                 |
| django_template            | 34.7 ms                                                | 44.3 ms: 1.28x slower                                                 |
| logging_format             | 7.35 us                                                | 9.40 us: 1.28x slower                                                 |
| chaos                      | 62.8 ms                                                | 80.4 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.70 ms: 1.30x slower                                                 |
| 2to3                       | 264 ms                                                 | 342 ms: 1.30x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 77.4 ms: 1.31x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.21 ms: 1.32x slower                                                 |
| thrift                     | 791 us                                                 | 1.05 ms: 1.33x slower                                                 |
| fannkuch                   | 372 ms                                                 | 498 ms: 1.34x slower                                                  |
| telco                      | 6.53 ms                                                | 8.74 ms: 1.34x slower                                                 |
| float                      | 80.8 ms                                                | 109 ms: 1.35x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.3 ms: 1.38x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.89 ms: 1.39x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 95.6 ms: 1.40x slower                                                 |
| scimark_sor                | 130 ms                                                 | 181 ms: 1.40x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 28.7 ms: 1.40x slower                                                 |
| richards                   | 45.9 ms                                                | 65.3 ms: 1.42x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 164 ms: 1.43x slower                                                  |
| richards_super             | 51.9 ms                                                | 74.7 ms: 1.44x slower                                                 |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| deltablue                  | 3.45 ms                                                | 5.43 ms: 1.58x slower                                                 |
| sympy_str                  | 292 ms                                                 | 460 ms: 1.58x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.78 ms: 1.63x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 14.2 ms: 1.99x slower                                                 |
| sympy_expand               | 468 ms                                                 | 933 ms: 1.99x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 343 ms: 2.06x slower                                                  |
| python_startup             | 9.93 ms                                                | 23.6 ms: 2.38x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.64x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 116 ms: 10.71x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.20x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241212-3.14.0a2+-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.136x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.34x