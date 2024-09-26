# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 2613a14
- commit date: 2024-09-25
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 412 ms: 1.59x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                               |
| html5lib       | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| tornado_http   | 114 ms                                                       | 158 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                        | 1.44x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 899 ms: 1.02x faster                                                 |
| asyncio_websockets        | 520 ms                                                       | 517 ms: 1.01x faster                                                 |
| async_tree_io             | 876 ms                                                       | 926 ms: 1.06x slower                                                 |
| async_tree_memoization    | 461 ms                                                       | 509 ms: 1.10x slower                                                 |
| async_tree_none_tg        | 336 ms                                                       | 380 ms: 1.13x slower                                                 |
| asyncio_tcp               | 505 ms                                                       | 574 ms: 1.13x slower                                                 |
| async_tree_memoization_tg | 414 ms                                                       | 476 ms: 1.15x slower                                                 |
| async_tree_none           | 354 ms                                                       | 415 ms: 1.17x slower                                                 |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.82 sec: 1.21x slower                                               |
| coroutines                | 23.6 ms                                                      | 28.6 ms: 1.21x slower                                                |
| async_generators          | 377 ms                                                       | 493 ms: 1.31x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.11x slower                                                         |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                 |
| float          | 77.5 ms                                                      | 146 ms: 1.89x slower                                                 |
| nbody          | 85.1 ms                                                      | 191 ms: 2.24x slower                                                 |
| Geometric mean | (ref)                                                        | 1.54x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.10 ms: 1.01x slower                                                |
| regex_dna      | 180 ms                                                       | 189 ms: 1.05x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                |
| regex_compile  | 132 ms                                                       | 213 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                        | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.7 us: 1.06x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.74 us: 1.04x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.01x slower                                                |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.05x slower                                                |
| json_loads           | 27.0 us                                                      | 28.9 us: 1.07x slower                                                |
| unpickle_list        | 4.71 us                                                      | 5.09 us: 1.08x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 103 ms: 1.08x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 108 ms: 1.26x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.6 ms: 1.29x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 87.3 ms: 1.47x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.06 sec: 1.53x slower                                               |
| unpickle_pure_python | 210 us                                                       | 387 us: 1.84x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 571 us: 1.94x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.21x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 75.1 ms: 1.54x slower                                                |
| genshi_text     | 21.5 ms                                                      | 36.2 ms: 1.68x slower                                                |
| django_template | 34.1 ms                                                      | 57.7 ms: 1.69x slower                                                |
| mako            | 11.3 ms                                                      | 19.9 ms: 1.76x slower                                                |
| Geometric mean  | (ref)                                                        | 1.67x slower                                                         |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal              | 3.14 ms                                                      | 2.54 ms: 1.24x faster                                                |
| create_gc_cycles          | 1.34 ms                                                      | 1.10 ms: 1.21x faster                                                |
| pidigits                  | 217 ms                                                       | 186 ms: 1.17x faster                                                 |
| pickle                    | 11.3 us                                                      | 10.7 us: 1.06x faster                                                |
| pickle_list               | 4.93 us                                                      | 4.74 us: 1.04x faster                                                |
| xml_etree_parse           | 136 ms                                                       | 132 ms: 1.03x faster                                                 |
| async_tree_io_tg          | 913 ms                                                       | 899 ms: 1.02x faster                                                 |
| asyncio_websockets        | 520 ms                                                       | 517 ms: 1.01x faster                                                 |
| regex_effbot              | 3.08 ms                                                      | 3.10 ms: 1.01x slower                                                |
| pickle_dict               | 32.5 us                                                      | 32.7 us: 1.01x slower                                                |
| unpickle                  | 14.3 us                                                      | 15.0 us: 1.05x slower                                                |
| regex_dna                 | 180 ms                                                       | 189 ms: 1.05x slower                                                 |
| async_tree_io             | 876 ms                                                       | 926 ms: 1.06x slower                                                 |
| json                      | 4.93 ms                                                      | 5.23 ms: 1.06x slower                                                |
| sqlite_synth              | 2.21 us                                                      | 2.35 us: 1.07x slower                                                |
| json_loads                | 27.0 us                                                      | 28.9 us: 1.07x slower                                                |
| regex_v8                  | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                |
| unpickle_list             | 4.71 us                                                      | 5.09 us: 1.08x slower                                                |
| xml_etree_iterparse       | 94.9 ms                                                      | 103 ms: 1.08x slower                                                 |
| deepcopy                  | 355 us                                                       | 386 us: 1.09x slower                                                 |
| pathlib                   | 19.2 ms                                                      | 21.0 ms: 1.09x slower                                                |
| async_tree_memoization    | 461 ms                                                       | 509 ms: 1.10x slower                                                 |
| async_tree_none_tg        | 336 ms                                                       | 380 ms: 1.13x slower                                                 |
| asyncio_tcp               | 505 ms                                                       | 574 ms: 1.13x slower                                                 |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.36 ms: 1.14x slower                                                |
| async_tree_memoization_tg | 414 ms                                                       | 476 ms: 1.15x slower                                                 |
| scimark_fft               | 349 ms                                                       | 402 ms: 1.15x slower                                                 |
| async_tree_none           | 354 ms                                                       | 415 ms: 1.17x slower                                                 |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.82 sec: 1.21x slower                                               |
| deepcopy_memo             | 39.1 us                                                      | 47.2 us: 1.21x slower                                                |
| coverage                  | 83.0 ms                                                      | 101 ms: 1.21x slower                                                 |
| coroutines                | 23.6 ms                                                      | 28.6 ms: 1.21x slower                                                |
| telco                     | 7.82 ms                                                      | 9.60 ms: 1.23x slower                                                |
| docutils                  | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                               |
| xml_etree_generate        | 85.4 ms                                                      | 108 ms: 1.26x slower                                                 |
| bench_mp_pool             | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                |
| pylint                    | 317 ms                                                       | 408 ms: 1.29x slower                                                 |
| json_dumps                | 10.5 ms                                                      | 13.6 ms: 1.29x slower                                                |
| async_generators          | 377 ms                                                       | 493 ms: 1.31x slower                                                 |
| deepcopy_reduce           | 3.11 us                                                      | 4.07 us: 1.31x slower                                                |
| mdp                       | 2.36 sec                                                     | 3.09 sec: 1.31x slower                                               |
| bpe_tokeniser             | 4.45 sec                                                     | 5.90 sec: 1.33x slower                                               |
| spectral_norm             | 111 ms                                                       | 148 ms: 1.34x slower                                                 |
| meteor_contest            | 102 ms                                                       | 137 ms: 1.35x slower                                                 |
| dulwich_log               | 74.8 ms                                                      | 101 ms: 1.35x slower                                                 |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| typing_runtime_protocols  | 155 us                                                       | 214 us: 1.39x slower                                                 |
| tornado_http              | 114 ms                                                       | 158 ms: 1.39x slower                                                 |
| nqueens                   | 78.6 ms                                                      | 111 ms: 1.42x slower                                                 |
| python_startup            | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                |
| generators                | 28.8 ms                                                      | 42.2 ms: 1.47x slower                                                |
| xml_etree_process         | 59.3 ms                                                      | 87.3 ms: 1.47x slower                                                |
| fannkuch                  | 370 ms                                                       | 558 ms: 1.51x slower                                                 |
| pycparser                 | 1.12 sec                                                     | 1.69 sec: 1.51x slower                                               |
| sqlglot_normalize         | 106 ms                                                       | 161 ms: 1.52x slower                                                 |
| tomli_loads               | 2.01 sec                                                     | 3.06 sec: 1.53x slower                                               |
| sqlglot_optimize          | 52.7 ms                                                      | 80.5 ms: 1.53x slower                                                |
| genshi_xml                | 48.8 ms                                                      | 75.1 ms: 1.54x slower                                                |
| html5lib                  | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| pprint_safe_repr          | 738 ms                                                       | 1.16 sec: 1.58x slower                                               |
| 2to3                      | 260 ms                                                       | 412 ms: 1.59x slower                                                 |
| sympy_integrate           | 19.8 ms                                                      | 31.7 ms: 1.60x slower                                                |
| regex_compile             | 132 ms                                                       | 213 ms: 1.61x slower                                                 |
| crypto_pyaes              | 67.9 ms                                                      | 109 ms: 1.61x slower                                                 |
| pprint_pformat            | 1.50 sec                                                     | 2.41 sec: 1.61x slower                                               |
| thrift                    | 778 us                                                       | 1.26 ms: 1.62x slower                                                |
| genshi_text               | 21.5 ms                                                      | 36.2 ms: 1.68x slower                                                |
| django_template           | 34.1 ms                                                      | 57.7 ms: 1.69x slower                                                |
| pyflate                   | 449 ms                                                       | 761 ms: 1.70x slower                                                 |
| mako                      | 11.3 ms                                                      | 19.9 ms: 1.76x slower                                                |
| comprehensions            | 16.5 us                                                      | 29.7 us: 1.80x slower                                                |
| unpickle_pure_python      | 210 us                                                       | 387 us: 1.84x slower                                                 |
| richards                  | 45.2 ms                                                      | 85.0 ms: 1.88x slower                                                |
| scimark_monte_carlo       | 65.4 ms                                                      | 123 ms: 1.88x slower                                                 |
| float                     | 77.5 ms                                                      | 146 ms: 1.89x slower                                                 |
| scimark_lu                | 113 ms                                                       | 213 ms: 1.89x slower                                                 |
| sympy_str                 | 275 ms                                                       | 522 ms: 1.90x slower                                                 |
| logging_format            | 6.84 us                                                      | 13.0 us: 1.90x slower                                                |
| logging_simple            | 6.16 us                                                      | 11.7 us: 1.91x slower                                                |
| pickle_pure_python        | 294 us                                                       | 571 us: 1.94x slower                                                 |
| hexiom                    | 5.99 ms                                                      | 11.7 ms: 1.96x slower                                                |
| richards_super            | 51.6 ms                                                      | 102 ms: 1.98x slower                                                 |
| scimark_sor               | 134 ms                                                       | 267 ms: 1.99x slower                                                 |
| logging_silent            | 103 ns                                                       | 206 ns: 2.00x slower                                                 |
| chaos                     | 57.3 ms                                                      | 117 ms: 2.05x slower                                                 |
| go                        | 141 ms                                                       | 290 ms: 2.06x slower                                                 |
| sqlglot_transpile         | 1.56 ms                                                      | 3.22 ms: 2.07x slower                                                |
| sqlglot_parse             | 1.25 ms                                                      | 2.79 ms: 2.23x slower                                                |
| nbody                     | 85.1 ms                                                      | 191 ms: 2.24x slower                                                 |
| sympy_expand              | 457 ms                                                       | 1.03 sec: 2.25x slower                                               |
| sympy_sum                 | 156 ms                                                       | 371 ms: 2.39x slower                                                 |
| raytrace                  | 253 ms                                                       | 628 ms: 2.49x slower                                                 |
| deltablue                 | 3.12 ms                                                      | 8.68 ms: 2.78x slower                                                |
| unpack_sequence           | 44.8 ns                                                      | 137 ns: 3.06x slower                                                 |
| bench_thread_pool         | 919 us                                                       | 3.16 ms: 3.44x slower                                                |
| Geometric mean            | (ref)                                                        | 1.43x slower                                                         |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.19x