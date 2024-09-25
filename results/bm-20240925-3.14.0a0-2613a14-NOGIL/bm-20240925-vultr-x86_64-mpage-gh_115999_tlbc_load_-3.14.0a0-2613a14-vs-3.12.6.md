# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 2613a14
- commit date: 2024-09-25
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 414 ms: 1.57x slower                                                 |
| docutils       | 2.64 sec                                               | 3.27 sec: 1.24x slower                                               |
| html5lib       | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| tornado_http   | 119 ms                                                 | 159 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                  | 1.43x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 897 ms: 1.24x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 477 ms: 1.17x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 381 ms: 1.17x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 925 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 637 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 420 ms: 1.10x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 512 ms: 1.08x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 676 ms: 1.06x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 573 ms: 1.11x slower                                                 |
| coroutines                 | 23.9 ms                                                | 28.7 ms: 1.20x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.82 sec: 1.21x slower                                               |
| async_generators           | 384 ms                                                 | 497 ms: 1.29x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| float          | 80.8 ms                                                | 146 ms: 1.81x slower                                                 |
| nbody          | 89.3 ms                                                | 188 ms: 2.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.57x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                 |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.17x slower                                                |
| regex_compile  | 142 ms                                                 | 212 ms: 1.49x slower                                                 |
| Geometric mean | (ref)                                                  | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 31.8 us                                                | 30.2 us: 1.05x faster                                                |
| pickle_list          | 4.77 us                                                | 4.56 us: 1.05x faster                                                |
| pickle               | 10.9 us                                                | 10.5 us: 1.04x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 103 ms: 1.06x slower                                                 |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.00 us: 1.07x slower                                                |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 107 ms: 1.26x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.28x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.07 sec: 1.45x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 87.2 ms: 1.48x slower                                                |
| unpickle_pure_python | 221 us                                                 | 384 us: 1.74x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 564 us: 1.83x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 75.1 ms: 1.50x slower                                                |
| genshi_text     | 22.8 ms                                                | 36.7 ms: 1.61x slower                                                |
| django_template | 34.7 ms                                                | 57.8 ms: 1.67x slower                                                |
| mako            | 11.0 ms                                                | 20.0 ms: 1.81x slower                                                |
| Geometric mean  | (ref)                                                  | 1.64x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 2.46 ms: 1.41x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 897 ms: 1.24x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 477 ms: 1.17x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 381 ms: 1.17x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 925 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 637 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 420 ms: 1.10x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 512 ms: 1.08x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 676 ms: 1.06x faster                                                 |
| pickle_dict                | 31.8 us                                                | 30.2 us: 1.05x faster                                                |
| pickle_list                | 4.77 us                                                | 4.56 us: 1.05x faster                                                |
| pickle                     | 10.9 us                                                | 10.5 us: 1.04x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                 |
| pathlib                    | 21.5 ms                                                | 21.1 ms: 1.02x faster                                                |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.11 ms: 1.02x slower                                                |
| json                       | 5.02 ms                                                | 5.25 ms: 1.05x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.33 us: 1.06x slower                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 103 ms: 1.06x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.0 us: 1.07x slower                                                |
| unpickle_list              | 4.67 us                                                | 5.00 us: 1.07x slower                                                |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                 |
| asyncio_tcp                | 519 ms                                                 | 573 ms: 1.11x slower                                                 |
| deepcopy                   | 352 us                                                 | 390 us: 1.11x slower                                                 |
| scimark_fft                | 342 ms                                                 | 397 ms: 1.16x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.17x slower                                                |
| deepcopy_memo              | 40.3 us                                                | 47.4 us: 1.18x slower                                                |
| coroutines                 | 23.9 ms                                                | 28.7 ms: 1.20x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.82 sec: 1.21x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.32 ms: 1.21x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 5.87 sec: 1.24x slower                                               |
| docutils                   | 2.64 sec                                               | 3.27 sec: 1.24x slower                                               |
| xml_etree_generate         | 85.2 ms                                                | 107 ms: 1.26x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.28x slower                                                |
| pylint                     | 319 ms                                                 | 408 ms: 1.28x slower                                                 |
| mdp                        | 2.42 sec                                               | 3.11 sec: 1.28x slower                                               |
| async_generators           | 384 ms                                                 | 497 ms: 1.29x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 14.0 ms: 1.29x slower                                                |
| dulwich_log                | 78.9 ms                                                | 102 ms: 1.30x slower                                                 |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.30x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 4.05 us: 1.32x slower                                                |
| spectral_norm              | 110 ms                                                 | 146 ms: 1.32x slower                                                 |
| tornado_http               | 119 ms                                                 | 159 ms: 1.33x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 219 us: 1.34x slower                                                 |
| generators                 | 32.2 ms                                                | 44.3 ms: 1.37x slower                                                |
| nqueens                    | 80.1 ms                                                | 112 ms: 1.39x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 107 ms: 1.40x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| coverage                   | 71.4 ms                                                | 103 ms: 1.44x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.69 sec: 1.44x slower                                               |
| tomli_loads                | 2.11 sec                                               | 3.07 sec: 1.45x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 87.2 ms: 1.48x slower                                                |
| comprehensions             | 19.8 us                                                | 29.5 us: 1.49x slower                                                |
| regex_compile              | 142 ms                                                 | 212 ms: 1.49x slower                                                 |
| fannkuch                   | 372 ms                                                 | 556 ms: 1.49x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 75.1 ms: 1.50x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 160 ms: 1.50x slower                                                 |
| telco                      | 6.53 ms                                                | 9.87 ms: 1.51x slower                                                |
| sqlglot_optimize           | 53.3 ms                                                | 80.7 ms: 1.52x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 31.8 ms: 1.55x slower                                                |
| 2to3                       | 264 ms                                                 | 414 ms: 1.57x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 1.18 sec: 1.59x slower                                               |
| thrift                     | 791 us                                                 | 1.26 ms: 1.59x slower                                                |
| genshi_text                | 22.8 ms                                                | 36.7 ms: 1.61x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 2.45 sec: 1.61x slower                                               |
| html5lib                   | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| django_template            | 34.7 ms                                                | 57.8 ms: 1.67x slower                                                |
| pyflate                    | 448 ms                                                 | 753 ms: 1.68x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 384 us: 1.74x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 122 ms: 1.78x slower                                                 |
| sympy_str                  | 292 ms                                                 | 523 ms: 1.79x slower                                                 |
| logging_format             | 7.35 us                                                | 13.2 us: 1.79x slower                                                |
| float                      | 80.8 ms                                                | 146 ms: 1.81x slower                                                 |
| logging_simple             | 6.63 us                                                | 12.0 us: 1.81x slower                                                |
| mako                       | 11.0 ms                                                | 20.0 ms: 1.81x slower                                                |
| pickle_pure_python         | 308 us                                                 | 564 us: 1.83x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 210 ms: 1.84x slower                                                 |
| chaos                      | 62.8 ms                                                | 116 ms: 1.85x slower                                                 |
| richards                   | 45.9 ms                                                | 85.3 ms: 1.86x slower                                                |
| logging_silent             | 109 ns                                                 | 204 ns: 1.87x slower                                                 |
| hexiom                     | 6.17 ms                                                | 11.6 ms: 1.88x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 3.23 ms: 1.93x slower                                                |
| richards_super             | 51.9 ms                                                | 102 ms: 1.96x slower                                                 |
| scimark_sor                | 130 ms                                                 | 264 ms: 2.03x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.81 ms: 2.07x slower                                                |
| go                         | 139 ms                                                 | 289 ms: 2.08x slower                                                 |
| raytrace                   | 299 ms                                                 | 623 ms: 2.08x slower                                                 |
| nbody                      | 89.3 ms                                                | 188 ms: 2.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 1.02 sec: 2.19x slower                                               |
| sympy_sum                  | 166 ms                                                 | 372 ms: 2.24x slower                                                 |
| deltablue                  | 3.45 ms                                                | 8.81 ms: 2.56x slower                                                |
| unpack_sequence            | 52.1 ns                                                | 141 ns: 2.71x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.17 ms: 3.36x slower                                                |
| Geometric mean             | (ref)                                                  | 1.38x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.21x