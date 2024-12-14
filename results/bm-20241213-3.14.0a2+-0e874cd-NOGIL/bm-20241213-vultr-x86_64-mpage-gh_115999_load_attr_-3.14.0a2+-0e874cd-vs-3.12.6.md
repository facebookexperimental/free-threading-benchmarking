# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 0e874cd
- commit date: 2024-12-13
- overall geometric mean: 1.120x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 323 ms: 1.23x slower                                                  |
| docutils       | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                |
| html5lib       | 63.6 ms                                                | 80.8 ms: 1.27x slower                                                 |
| Geometric mean | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 635 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 271 ms: 1.65x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 668 ms: 1.62x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 346 ms: 1.62x faster                                                  |
| async_tree_none            | 464 ms                                                 | 311 ms: 1.49x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 380 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 515 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.03x slower                                                 |
| async_generators           | 384 ms                                                 | 421 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 104 ms: 1.29x slower                                                  |
| nbody          | 89.3 ms                                                | 129 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| regex_compile  | 142 ms                                                 | 159 ms: 1.12x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.1 ms: 1.12x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 256 us: 1.16x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.53 sec: 1.20x slower                                                |
| pickle_pure_python   | 308 us                                                 | 372 us: 1.21x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 71.5 ms: 1.21x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 61.0 ms: 1.22x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                 |
| django_template | 34.7 ms                                                | 43.6 ms: 1.26x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 635 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 271 ms: 1.65x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 668 ms: 1.62x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 346 ms: 1.62x faster                                                  |
| async_tree_none            | 464 ms                                                 | 311 ms: 1.49x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 380 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 515 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.19 ms: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.6 us: 1.04x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.11 us: 1.04x faster                                                 |
| generators                 | 32.2 ms                                                | 31.2 ms: 1.03x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.76 sec: 1.00x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.9 us: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| logging_silent             | 109 ns                                                 | 116 ns: 1.06x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 86.0 ms: 1.09x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                |
| pylint                     | 319 ms                                                 | 349 ms: 1.10x slower                                                  |
| async_generators           | 384 ms                                                 | 421 ms: 1.10x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.39 us: 1.10x slower                                                 |
| scimark_fft                | 342 ms                                                 | 379 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.1 ms: 1.12x slower                                                 |
| regex_compile              | 142 ms                                                 | 159 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.1 ms: 1.12x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.6 ms: 1.13x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.76 sec: 1.14x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.35 sec: 1.15x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 256 us: 1.16x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.8 ms: 1.16x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 874 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.80 sec: 1.18x slower                                                |
| pyflate                    | 448 ms                                                 | 530 ms: 1.18x slower                                                  |
| go                         | 139 ms                                                 | 167 ms: 1.20x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.53 sec: 1.20x slower                                                |
| pickle_pure_python         | 308 us                                                 | 372 us: 1.21x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 71.5 ms: 1.21x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 61.0 ms: 1.22x slower                                                 |
| logging_simple             | 6.63 us                                                | 8.09 us: 1.22x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                  |
| 2to3                       | 264 ms                                                 | 323 ms: 1.23x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                 |
| nqueens                    | 80.1 ms                                                | 98.7 ms: 1.23x slower                                                 |
| logging_format             | 7.35 us                                                | 9.10 us: 1.24x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 178 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| django_template            | 34.7 ms                                                | 43.6 ms: 1.26x slower                                                 |
| chaos                      | 62.8 ms                                                | 79.0 ms: 1.26x slower                                                 |
| raytrace                   | 299 ms                                                 | 376 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.53 ms: 1.26x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                 |
| html5lib                   | 63.6 ms                                                | 80.8 ms: 1.27x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.90 ms: 1.28x slower                                                 |
| telco                      | 6.53 ms                                                | 8.36 ms: 1.28x slower                                                 |
| float                      | 80.8 ms                                                | 104 ms: 1.29x slower                                                  |
| thrift                     | 791 us                                                 | 1.04 ms: 1.31x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.20 ms: 1.32x slower                                                 |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.7 ms: 1.38x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.88 ms: 1.38x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 94.9 ms: 1.39x slower                                                 |
| scimark_sor                | 130 ms                                                 | 181 ms: 1.40x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 28.7 ms: 1.40x slower                                                 |
| richards                   | 45.9 ms                                                | 65.0 ms: 1.42x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| richards_super             | 51.9 ms                                                | 74.0 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| nbody                      | 89.3 ms                                                | 129 ms: 1.45x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 166 ms: 1.46x slower                                                  |
| deltablue                  | 3.45 ms                                                | 5.43 ms: 1.58x slower                                                 |
| sympy_str                  | 292 ms                                                 | 461 ms: 1.58x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                 |
| sympy_expand               | 468 ms                                                 | 934 ms: 2.00x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 342 ms: 2.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.35 ms: 3.56x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 106 ms: 9.83x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.18x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.120x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.34x