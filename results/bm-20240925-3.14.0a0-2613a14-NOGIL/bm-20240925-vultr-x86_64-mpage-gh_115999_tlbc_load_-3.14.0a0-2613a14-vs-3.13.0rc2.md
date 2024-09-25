# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 2613a14
- commit date: 2024-09-25
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 414 ms: 1.59x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.27 sec: 1.25x slower                                               |
| html5lib       | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| tornado_http   | 114 ms                                                       | 159 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                        | 1.44x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 897 ms: 1.02x faster                                                 |
| asyncio_websockets        | 520 ms                                                       | 518 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 676 ms: 1.01x slower                                                 |
| async_tree_io             | 876 ms                                                       | 925 ms: 1.06x slower                                                 |
| async_tree_memoization    | 461 ms                                                       | 512 ms: 1.11x slower                                                 |
| async_tree_none_tg        | 336 ms                                                       | 381 ms: 1.13x slower                                                 |
| asyncio_tcp               | 505 ms                                                       | 573 ms: 1.13x slower                                                 |
| async_tree_memoization_tg | 414 ms                                                       | 477 ms: 1.15x slower                                                 |
| async_tree_none           | 354 ms                                                       | 420 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.82 sec: 1.21x slower                                               |
| coroutines                | 23.6 ms                                                      | 28.7 ms: 1.22x slower                                                |
| async_generators          | 377 ms                                                       | 497 ms: 1.32x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.11x slower                                                         |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                 |
| float          | 77.5 ms                                                      | 146 ms: 1.88x slower                                                 |
| nbody          | 85.1 ms                                                      | 188 ms: 2.21x slower                                                 |
| Geometric mean | (ref)                                                        | 1.53x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.96 ms: 1.04x faster                                                |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                |
| regex_compile  | 132 ms                                                       | 212 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                        | 1.14x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 4.93 us                                                      | 4.56 us: 1.08x faster                                                |
| pickle_dict          | 32.5 us                                                      | 30.2 us: 1.08x faster                                                |
| pickle               | 11.3 us                                                      | 10.5 us: 1.08x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                 |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.05x slower                                                |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                |
| unpickle_list        | 4.71 us                                                      | 5.00 us: 1.06x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 103 ms: 1.08x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 107 ms: 1.26x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 87.2 ms: 1.47x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.07 sec: 1.53x slower                                               |
| unpickle_pure_python | 210 us                                                       | 384 us: 1.83x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 564 us: 1.92x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                         |

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
| django_template | 34.1 ms                                                      | 57.8 ms: 1.69x slower                                                |
| genshi_text     | 21.5 ms                                                      | 36.7 ms: 1.71x slower                                                |
| mako            | 11.3 ms                                                      | 20.0 ms: 1.76x slower                                                |
| Geometric mean  | (ref)                                                        | 1.67x slower                                                         |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal              | 3.14 ms                                                      | 2.46 ms: 1.28x faster                                                |
| create_gc_cycles          | 1.34 ms                                                      | 1.11 ms: 1.20x faster                                                |
| pidigits                  | 217 ms                                                       | 186 ms: 1.17x faster                                                 |
| pickle_list               | 4.93 us                                                      | 4.56 us: 1.08x faster                                                |
| pickle_dict               | 32.5 us                                                      | 30.2 us: 1.08x faster                                                |
| pickle                    | 11.3 us                                                      | 10.5 us: 1.08x faster                                                |
| regex_effbot              | 3.08 ms                                                      | 2.96 ms: 1.04x faster                                                |
| xml_etree_parse           | 136 ms                                                       | 134 ms: 1.02x faster                                                 |
| async_tree_io_tg          | 913 ms                                                       | 897 ms: 1.02x faster                                                 |
| asyncio_websockets        | 520 ms                                                       | 518 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 676 ms: 1.01x slower                                                 |
| regex_dna                 | 180 ms                                                       | 184 ms: 1.02x slower                                                 |
| unpickle                  | 14.3 us                                                      | 15.0 us: 1.05x slower                                                |
| async_tree_io             | 876 ms                                                       | 925 ms: 1.06x slower                                                 |
| sqlite_synth              | 2.21 us                                                      | 2.33 us: 1.06x slower                                                |
| json_loads                | 27.0 us                                                      | 28.6 us: 1.06x slower                                                |
| unpickle_list             | 4.71 us                                                      | 5.00 us: 1.06x slower                                                |
| regex_v8                  | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                |
| json                      | 4.93 ms                                                      | 5.25 ms: 1.07x slower                                                |
| xml_etree_iterparse       | 94.9 ms                                                      | 103 ms: 1.08x slower                                                 |
| deepcopy                  | 355 us                                                       | 390 us: 1.10x slower                                                 |
| pathlib                   | 19.2 ms                                                      | 21.1 ms: 1.10x slower                                                |
| async_tree_memoization    | 461 ms                                                       | 512 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.32 ms: 1.13x slower                                                |
| async_tree_none_tg        | 336 ms                                                       | 381 ms: 1.13x slower                                                 |
| asyncio_tcp               | 505 ms                                                       | 573 ms: 1.13x slower                                                 |
| scimark_fft               | 349 ms                                                       | 397 ms: 1.14x slower                                                 |
| async_tree_memoization_tg | 414 ms                                                       | 477 ms: 1.15x slower                                                 |
| async_tree_none           | 354 ms                                                       | 420 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.82 sec: 1.21x slower                                               |
| deepcopy_memo             | 39.1 us                                                      | 47.4 us: 1.21x slower                                                |
| coroutines                | 23.6 ms                                                      | 28.7 ms: 1.22x slower                                                |
| coverage                  | 83.0 ms                                                      | 103 ms: 1.24x slower                                                 |
| docutils                  | 2.62 sec                                                     | 3.27 sec: 1.25x slower                                               |
| json_dumps                | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                                |
| xml_etree_generate        | 85.4 ms                                                      | 107 ms: 1.26x slower                                                 |
| telco                     | 7.82 ms                                                      | 9.87 ms: 1.26x slower                                                |
| bench_mp_pool             | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                |
| pylint                    | 317 ms                                                       | 408 ms: 1.29x slower                                                 |
| deepcopy_reduce           | 3.11 us                                                      | 4.05 us: 1.30x slower                                                |
| spectral_norm             | 111 ms                                                       | 146 ms: 1.31x slower                                                 |
| async_generators          | 377 ms                                                       | 497 ms: 1.32x slower                                                 |
| bpe_tokeniser             | 4.45 sec                                                     | 5.87 sec: 1.32x slower                                               |
| mdp                       | 2.36 sec                                                     | 3.11 sec: 1.32x slower                                               |
| meteor_contest            | 102 ms                                                       | 135 ms: 1.32x slower                                                 |
| dulwich_log               | 74.8 ms                                                      | 102 ms: 1.37x slower                                                 |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| tornado_http              | 114 ms                                                       | 159 ms: 1.39x slower                                                 |
| typing_runtime_protocols  | 155 us                                                       | 219 us: 1.42x slower                                                 |
| nqueens                   | 78.6 ms                                                      | 112 ms: 1.42x slower                                                 |
| python_startup            | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                |
| xml_etree_process         | 59.3 ms                                                      | 87.2 ms: 1.47x slower                                                |
| fannkuch                  | 370 ms                                                       | 556 ms: 1.50x slower                                                 |
| pycparser                 | 1.12 sec                                                     | 1.69 sec: 1.51x slower                                               |
| sqlglot_normalize         | 106 ms                                                       | 160 ms: 1.51x slower                                                 |
| tomli_loads               | 2.01 sec                                                     | 3.07 sec: 1.53x slower                                               |
| sqlglot_optimize          | 52.7 ms                                                      | 80.7 ms: 1.53x slower                                                |
| generators                | 28.8 ms                                                      | 44.3 ms: 1.54x slower                                                |
| genshi_xml                | 48.8 ms                                                      | 75.1 ms: 1.54x slower                                                |
| html5lib                  | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| crypto_pyaes              | 67.9 ms                                                      | 107 ms: 1.58x slower                                                 |
| 2to3                      | 260 ms                                                       | 414 ms: 1.59x slower                                                 |
| pprint_safe_repr          | 738 ms                                                       | 1.18 sec: 1.60x slower                                               |
| sympy_integrate           | 19.8 ms                                                      | 31.8 ms: 1.60x slower                                                |
| regex_compile             | 132 ms                                                       | 212 ms: 1.61x slower                                                 |
| thrift                    | 778 us                                                       | 1.26 ms: 1.62x slower                                                |
| pprint_pformat            | 1.50 sec                                                     | 2.45 sec: 1.64x slower                                               |
| pyflate                   | 449 ms                                                       | 753 ms: 1.68x slower                                                 |
| django_template           | 34.1 ms                                                      | 57.8 ms: 1.69x slower                                                |
| genshi_text               | 21.5 ms                                                      | 36.7 ms: 1.71x slower                                                |
| mako                      | 11.3 ms                                                      | 20.0 ms: 1.76x slower                                                |
| comprehensions            | 16.5 us                                                      | 29.5 us: 1.80x slower                                                |
| unpickle_pure_python      | 210 us                                                       | 384 us: 1.83x slower                                                 |
| scimark_monte_carlo       | 65.4 ms                                                      | 122 ms: 1.86x slower                                                 |
| scimark_lu                | 113 ms                                                       | 210 ms: 1.87x slower                                                 |
| float                     | 77.5 ms                                                      | 146 ms: 1.88x slower                                                 |
| richards                  | 45.2 ms                                                      | 85.3 ms: 1.89x slower                                                |
| sympy_str                 | 275 ms                                                       | 523 ms: 1.90x slower                                                 |
| pickle_pure_python        | 294 us                                                       | 564 us: 1.92x slower                                                 |
| logging_format            | 6.84 us                                                      | 13.2 us: 1.93x slower                                                |
| hexiom                    | 5.99 ms                                                      | 11.6 ms: 1.93x slower                                                |
| logging_simple            | 6.16 us                                                      | 12.0 us: 1.95x slower                                                |
| scimark_sor               | 134 ms                                                       | 264 ms: 1.96x slower                                                 |
| richards_super            | 51.6 ms                                                      | 102 ms: 1.97x slower                                                 |
| logging_silent            | 103 ns                                                       | 204 ns: 1.99x slower                                                 |
| chaos                     | 57.3 ms                                                      | 116 ms: 2.03x slower                                                 |
| go                        | 141 ms                                                       | 289 ms: 2.06x slower                                                 |
| sqlglot_transpile         | 1.56 ms                                                      | 3.23 ms: 2.07x slower                                                |
| nbody                     | 85.1 ms                                                      | 188 ms: 2.21x slower                                                 |
| sympy_expand              | 457 ms                                                       | 1.02 sec: 2.24x slower                                               |
| sqlglot_parse             | 1.25 ms                                                      | 2.81 ms: 2.25x slower                                                |
| sympy_sum                 | 156 ms                                                       | 372 ms: 2.39x slower                                                 |
| raytrace                  | 253 ms                                                       | 623 ms: 2.46x slower                                                 |
| deltablue                 | 3.12 ms                                                      | 8.81 ms: 2.82x slower                                                |
| unpack_sequence           | 44.8 ns                                                      | 141 ns: 3.15x slower                                                 |
| bench_thread_pool         | 919 us                                                       | 3.17 ms: 3.45x slower                                                |
| Geometric mean            | (ref)                                                        | 1.43x slower                                                         |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.19x