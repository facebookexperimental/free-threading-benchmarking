# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 2613a14
- commit date: 2024-09-25
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 412 ms: 1.56x slower                                                 |
| docutils       | 2.64 sec                                               | 3.29 sec: 1.25x slower                                               |
| html5lib       | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| tornado_http   | 119 ms                                                 | 158 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                  | 1.43x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 899 ms: 1.23x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 476 ms: 1.18x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 380 ms: 1.17x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 926 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 640 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 415 ms: 1.12x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 509 ms: 1.09x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 671 ms: 1.07x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                                 |
| coroutines                 | 23.9 ms                                                | 28.6 ms: 1.19x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.82 sec: 1.21x slower                                               |
| async_generators           | 384 ms                                                 | 493 ms: 1.28x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| float          | 80.8 ms                                                | 146 ms: 1.81x slower                                                 |
| nbody          | 89.3 ms                                                | 191 ms: 2.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.57x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.10 ms: 1.02x faster                                                |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                 |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                |
| regex_compile  | 142 ms                                                 | 213 ms: 1.49x slower                                                 |
| Geometric mean | (ref)                                                  | 1.18x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                 |
| pickle               | 10.9 us                                                | 10.7 us: 1.03x faster                                                |
| pickle_list          | 4.77 us                                                | 4.74 us: 1.01x faster                                                |
| pickle_dict          | 31.8 us                                                | 32.7 us: 1.03x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 103 ms: 1.06x slower                                                 |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                                |
| json_loads           | 26.5 us                                                | 28.9 us: 1.09x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.09 us: 1.09x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 108 ms: 1.27x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.6 ms: 1.31x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.06 sec: 1.45x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 87.3 ms: 1.48x slower                                                |
| unpickle_pure_python | 221 us                                                 | 387 us: 1.76x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 571 us: 1.86x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                         |

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
| genshi_text     | 22.8 ms                                                | 36.2 ms: 1.59x slower                                                |
| django_template | 34.7 ms                                                | 57.7 ms: 1.66x slower                                                |
| mako            | 11.0 ms                                                | 19.9 ms: 1.81x slower                                                |
| Geometric mean  | (ref)                                                  | 1.64x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 2.54 ms: 1.36x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 899 ms: 1.23x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 476 ms: 1.18x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 380 ms: 1.17x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 926 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 640 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 415 ms: 1.12x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 509 ms: 1.09x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 671 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                 |
| pickle                     | 10.9 us                                                | 10.7 us: 1.03x faster                                                |
| pathlib                    | 21.5 ms                                                | 21.0 ms: 1.03x faster                                                |
| regex_effbot               | 3.17 ms                                                | 3.10 ms: 1.02x faster                                                |
| pickle_list                | 4.77 us                                                | 4.74 us: 1.01x faster                                                |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.10 ms: 1.01x slower                                                |
| pickle_dict                | 31.8 us                                                | 32.7 us: 1.03x slower                                                |
| json                       | 5.02 ms                                                | 5.23 ms: 1.04x slower                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 103 ms: 1.06x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.0 us: 1.07x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.35 us: 1.07x slower                                                |
| json_loads                 | 26.5 us                                                | 28.9 us: 1.09x slower                                                |
| unpickle_list              | 4.67 us                                                | 5.09 us: 1.09x slower                                                |
| deepcopy                   | 352 us                                                 | 386 us: 1.10x slower                                                 |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                                 |
| regex_dna                  | 168 ms                                                 | 189 ms: 1.13x slower                                                 |
| deepcopy_memo              | 40.3 us                                                | 47.2 us: 1.17x slower                                                |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                |
| coroutines                 | 23.9 ms                                                | 28.6 ms: 1.19x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.82 sec: 1.21x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.36 ms: 1.22x slower                                                |
| docutils                   | 2.64 sec                                               | 3.29 sec: 1.25x slower                                               |
| bpe_tokeniser              | 4.74 sec                                               | 5.90 sec: 1.25x slower                                               |
| xml_etree_generate         | 85.2 ms                                                | 108 ms: 1.27x slower                                                 |
| mdp                        | 2.42 sec                                               | 3.09 sec: 1.28x slower                                               |
| pylint                     | 319 ms                                                 | 408 ms: 1.28x slower                                                 |
| async_generators           | 384 ms                                                 | 493 ms: 1.28x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 101 ms: 1.28x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 14.0 ms: 1.29x slower                                                |
| json_dumps                 | 10.4 ms                                                | 13.6 ms: 1.31x slower                                                |
| generators                 | 32.2 ms                                                | 42.2 ms: 1.31x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 214 us: 1.31x slower                                                 |
| meteor_contest             | 104 ms                                                 | 137 ms: 1.32x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 4.07 us: 1.32x slower                                                |
| tornado_http               | 119 ms                                                 | 158 ms: 1.33x slower                                                 |
| spectral_norm              | 110 ms                                                 | 148 ms: 1.35x slower                                                 |
| nqueens                    | 80.1 ms                                                | 111 ms: 1.39x slower                                                 |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 109 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.69 sec: 1.44x slower                                               |
| tomli_loads                | 2.11 sec                                               | 3.06 sec: 1.45x slower                                               |
| telco                      | 6.53 ms                                                | 9.60 ms: 1.47x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 87.3 ms: 1.48x slower                                                |
| regex_compile              | 142 ms                                                 | 213 ms: 1.49x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 75.1 ms: 1.50x slower                                                |
| comprehensions             | 19.8 us                                                | 29.7 us: 1.50x slower                                                |
| fannkuch                   | 372 ms                                                 | 558 ms: 1.50x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 161 ms: 1.51x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 80.5 ms: 1.51x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 31.7 ms: 1.54x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 1.16 sec: 1.56x slower                                               |
| 2to3                       | 264 ms                                                 | 412 ms: 1.56x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                |
| genshi_text                | 22.8 ms                                                | 36.2 ms: 1.59x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 2.41 sec: 1.59x slower                                               |
| thrift                     | 791 us                                                 | 1.26 ms: 1.59x slower                                                |
| html5lib                   | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| django_template            | 34.7 ms                                                | 57.7 ms: 1.66x slower                                                |
| pyflate                    | 448 ms                                                 | 761 ms: 1.70x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 387 us: 1.76x slower                                                 |
| logging_format             | 7.35 us                                                | 13.0 us: 1.77x slower                                                |
| logging_simple             | 6.63 us                                                | 11.7 us: 1.77x slower                                                |
| sympy_str                  | 292 ms                                                 | 522 ms: 1.79x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.80x slower                                                 |
| float                      | 80.8 ms                                                | 146 ms: 1.81x slower                                                 |
| mako                       | 11.0 ms                                                | 19.9 ms: 1.81x slower                                                |
| richards                   | 45.9 ms                                                | 85.0 ms: 1.85x slower                                                |
| pickle_pure_python         | 308 us                                                 | 571 us: 1.86x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 213 ms: 1.87x slower                                                 |
| chaos                      | 62.8 ms                                                | 117 ms: 1.87x slower                                                 |
| logging_silent             | 109 ns                                                 | 206 ns: 1.89x slower                                                 |
| hexiom                     | 6.17 ms                                                | 11.7 ms: 1.90x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 3.22 ms: 1.93x slower                                                |
| richards_super             | 51.9 ms                                                | 102 ms: 1.97x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.79 ms: 2.06x slower                                                |
| scimark_sor                | 130 ms                                                 | 267 ms: 2.06x slower                                                 |
| go                         | 139 ms                                                 | 290 ms: 2.09x slower                                                 |
| raytrace                   | 299 ms                                                 | 628 ms: 2.10x slower                                                 |
| nbody                      | 89.3 ms                                                | 191 ms: 2.14x slower                                                 |
| sympy_expand               | 468 ms                                                 | 1.03 sec: 2.20x slower                                               |
| sympy_sum                  | 166 ms                                                 | 371 ms: 2.24x slower                                                 |
| deltablue                  | 3.45 ms                                                | 8.68 ms: 2.52x slower                                                |
| unpack_sequence            | 52.1 ns                                                | 137 ns: 2.64x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.21x