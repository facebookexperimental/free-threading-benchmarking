# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: 2f11cc7
- commit date: 2024-09-17
- overall geometric mean: 1.47x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 414 ms: 1.59x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.34 sec: 1.28x slower                                               |
| html5lib       | 67.0 ms                                                      | 103 ms: 1.54x slower                                                 |
| tornado_http   | 114 ms                                                       | 162 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                        | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets        | 520 ms                                                       | 516 ms: 1.01x faster                                                 |
| async_tree_io             | 876 ms                                                       | 941 ms: 1.07x slower                                                 |
| async_tree_memoization    | 461 ms                                                       | 510 ms: 1.11x slower                                                 |
| async_tree_none_tg        | 336 ms                                                       | 379 ms: 1.13x slower                                                 |
| asyncio_tcp               | 505 ms                                                       | 574 ms: 1.14x slower                                                 |
| async_tree_memoization_tg | 414 ms                                                       | 475 ms: 1.15x slower                                                 |
| async_tree_none           | 354 ms                                                       | 420 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                               |
| coroutines                | 23.6 ms                                                      | 29.8 ms: 1.26x slower                                                |
| async_generators          | 377 ms                                                       | 493 ms: 1.31x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.12x slower                                                         |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| float          | 77.5 ms                                                      | 148 ms: 1.91x slower                                                 |
| nbody          | 85.1 ms                                                      | 185 ms: 2.17x slower                                                 |
| Geometric mean | (ref)                                                        | 1.52x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 196 ms: 1.09x slower                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.36 ms: 1.09x slower                                                |
| regex_v8       | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                |
| regex_compile  | 132 ms                                                       | 223 ms: 1.69x slower                                                 |
| Geometric mean | (ref)                                                        | 1.23x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                                |
| pickle               | 11.3 us                                                      | 11.1 us: 1.02x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.85 us: 1.02x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 135 ms: 1.01x faster                                                 |
| unpickle             | 14.3 us                                                      | 15.2 us: 1.06x slower                                                |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| unpickle_list        | 4.71 us                                                      | 5.05 us: 1.07x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 107 ms: 1.13x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.7 ms: 1.30x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 112 ms: 1.31x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 91.8 ms: 1.55x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.17 sec: 1.58x slower                                               |
| unpickle_pure_python | 210 us                                                       | 412 us: 1.96x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 604 us: 2.05x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 80.9 ms: 1.66x slower                                                |
| mako            | 11.3 ms                                                      | 20.3 ms: 1.79x slower                                                |
| genshi_text     | 21.5 ms                                                      | 39.8 ms: 1.85x slower                                                |
| django_template | 34.1 ms                                                      | 63.5 ms: 1.86x slower                                                |
| Geometric mean  | (ref)                                                        | 1.79x slower                                                         |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal              | 3.14 ms                                                      | 2.45 ms: 1.28x faster                                                |
| create_gc_cycles          | 1.34 ms                                                      | 1.11 ms: 1.20x faster                                                |
| pidigits                  | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| pickle_dict               | 32.5 us                                                      | 31.6 us: 1.03x faster                                                |
| pickle                    | 11.3 us                                                      | 11.1 us: 1.02x faster                                                |
| pickle_list               | 4.93 us                                                      | 4.85 us: 1.02x faster                                                |
| xml_etree_parse           | 136 ms                                                       | 135 ms: 1.01x faster                                                 |
| asyncio_websockets        | 520 ms                                                       | 516 ms: 1.01x faster                                                 |
| unpickle                  | 14.3 us                                                      | 15.2 us: 1.06x slower                                                |
| json_loads                | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| unpickle_list             | 4.71 us                                                      | 5.05 us: 1.07x slower                                                |
| async_tree_io             | 876 ms                                                       | 941 ms: 1.07x slower                                                 |
| json                      | 4.93 ms                                                      | 5.31 ms: 1.08x slower                                                |
| sqlite_synth              | 2.21 us                                                      | 2.40 us: 1.09x slower                                                |
| regex_dna                 | 180 ms                                                       | 196 ms: 1.09x slower                                                 |
| regex_effbot              | 3.08 ms                                                      | 3.36 ms: 1.09x slower                                                |
| scimark_fft               | 349 ms                                                       | 386 ms: 1.11x slower                                                 |
| async_tree_memoization    | 461 ms                                                       | 510 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.21 ms: 1.11x slower                                                |
| pathlib                   | 19.2 ms                                                      | 21.6 ms: 1.13x slower                                                |
| async_tree_none_tg        | 336 ms                                                       | 379 ms: 1.13x slower                                                 |
| xml_etree_iterparse       | 94.9 ms                                                      | 107 ms: 1.13x slower                                                 |
| asyncio_tcp               | 505 ms                                                       | 574 ms: 1.14x slower                                                 |
| regex_v8                  | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                |
| async_tree_memoization_tg | 414 ms                                                       | 475 ms: 1.15x slower                                                 |
| async_tree_none           | 354 ms                                                       | 420 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                               |
| deepcopy                  | 355 us                                                       | 435 us: 1.22x slower                                                 |
| telco                     | 7.82 ms                                                      | 9.57 ms: 1.22x slower                                                |
| coverage                  | 83.0 ms                                                      | 103 ms: 1.24x slower                                                 |
| coroutines                | 23.6 ms                                                      | 29.8 ms: 1.26x slower                                                |
| bench_mp_pool             | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                |
| docutils                  | 2.62 sec                                                     | 3.34 sec: 1.28x slower                                               |
| json_dumps                | 10.5 ms                                                      | 13.7 ms: 1.30x slower                                                |
| async_generators          | 377 ms                                                       | 493 ms: 1.31x slower                                                 |
| xml_etree_generate        | 85.4 ms                                                      | 112 ms: 1.31x slower                                                 |
| spectral_norm             | 111 ms                                                       | 146 ms: 1.31x slower                                                 |
| pylint                    | 317 ms                                                       | 420 ms: 1.32x slower                                                 |
| mdp                       | 2.36 sec                                                     | 3.17 sec: 1.35x slower                                               |
| meteor_contest            | 102 ms                                                       | 138 ms: 1.36x slower                                                 |
| dulwich_log               | 74.8 ms                                                      | 102 ms: 1.36x slower                                                 |
| bpe_tokeniser             | 4.45 sec                                                     | 6.12 sec: 1.38x slower                                               |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                |
| tornado_http              | 114 ms                                                       | 162 ms: 1.42x slower                                                 |
| python_startup            | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                |
| deepcopy_memo             | 39.1 us                                                      | 56.0 us: 1.43x slower                                                |
| nqueens                   | 78.6 ms                                                      | 114 ms: 1.45x slower                                                 |
| generators                | 28.8 ms                                                      | 42.0 ms: 1.46x slower                                                |
| deepcopy_reduce           | 3.11 us                                                      | 4.54 us: 1.46x slower                                                |
| fannkuch                  | 370 ms                                                       | 551 ms: 1.49x slower                                                 |
| pycparser                 | 1.12 sec                                                     | 1.69 sec: 1.51x slower                                               |
| html5lib                  | 67.0 ms                                                      | 103 ms: 1.54x slower                                                 |
| xml_etree_process         | 59.3 ms                                                      | 91.8 ms: 1.55x slower                                                |
| crypto_pyaes              | 67.9 ms                                                      | 107 ms: 1.57x slower                                                 |
| tomli_loads               | 2.01 sec                                                     | 3.17 sec: 1.58x slower                                               |
| typing_runtime_protocols  | 155 us                                                       | 245 us: 1.58x slower                                                 |
| 2to3                      | 260 ms                                                       | 414 ms: 1.59x slower                                                 |
| thrift                    | 778 us                                                       | 1.27 ms: 1.63x slower                                                |
| sympy_integrate           | 19.8 ms                                                      | 32.5 ms: 1.64x slower                                                |
| genshi_xml                | 48.8 ms                                                      | 80.9 ms: 1.66x slower                                                |
| regex_compile             | 132 ms                                                       | 223 ms: 1.69x slower                                                 |
| sqlglot_normalize         | 106 ms                                                       | 179 ms: 1.70x slower                                                 |
| sqlglot_optimize          | 52.7 ms                                                      | 90.0 ms: 1.71x slower                                                |
| pyflate                   | 449 ms                                                       | 769 ms: 1.72x slower                                                 |
| pprint_safe_repr          | 738 ms                                                       | 1.32 sec: 1.79x slower                                               |
| mako                      | 11.3 ms                                                      | 20.3 ms: 1.79x slower                                                |
| comprehensions            | 16.5 us                                                      | 29.9 us: 1.82x slower                                                |
| pprint_pformat            | 1.50 sec                                                     | 2.74 sec: 1.83x slower                                               |
| genshi_text               | 21.5 ms                                                      | 39.8 ms: 1.85x slower                                                |
| django_template           | 34.1 ms                                                      | 63.5 ms: 1.86x slower                                                |
| scimark_monte_carlo       | 65.4 ms                                                      | 122 ms: 1.87x slower                                                 |
| scimark_sor               | 134 ms                                                       | 256 ms: 1.91x slower                                                 |
| float                     | 77.5 ms                                                      | 148 ms: 1.91x slower                                                 |
| sympy_str                 | 275 ms                                                       | 535 ms: 1.95x slower                                                 |
| logging_format            | 6.84 us                                                      | 13.4 us: 1.96x slower                                                |
| unpickle_pure_python      | 210 us                                                       | 412 us: 1.96x slower                                                 |
| richards                  | 45.2 ms                                                      | 89.1 ms: 1.97x slower                                                |
| logging_simple            | 6.16 us                                                      | 12.2 us: 1.99x slower                                                |
| hexiom                    | 5.99 ms                                                      | 12.1 ms: 2.03x slower                                                |
| pickle_pure_python        | 294 us                                                       | 604 us: 2.05x slower                                                 |
| chaos                     | 57.3 ms                                                      | 118 ms: 2.05x slower                                                 |
| richards_super            | 51.6 ms                                                      | 107 ms: 2.07x slower                                                 |
| go                        | 141 ms                                                       | 294 ms: 2.09x slower                                                 |
| sqlglot_transpile         | 1.56 ms                                                      | 3.28 ms: 2.10x slower                                                |
| logging_silent            | 103 ns                                                       | 218 ns: 2.12x slower                                                 |
| scimark_lu                | 113 ms                                                       | 240 ms: 2.13x slower                                                 |
| nbody                     | 85.1 ms                                                      | 185 ms: 2.17x slower                                                 |
| sqlglot_parse             | 1.25 ms                                                      | 2.85 ms: 2.28x slower                                                |
| sympy_expand              | 457 ms                                                       | 1.05 sec: 2.29x slower                                               |
| sympy_sum                 | 156 ms                                                       | 380 ms: 2.44x slower                                                 |
| raytrace                  | 253 ms                                                       | 626 ms: 2.48x slower                                                 |
| deltablue                 | 3.12 ms                                                      | 9.04 ms: 2.90x slower                                                |
| unpack_sequence           | 44.8 ns                                                      | 133 ns: 2.97x slower                                                 |
| bench_thread_pool         | 919 us                                                       | 3.18 ms: 3.46x slower                                                |
| Geometric mean            | (ref)                                                        | 1.47x slower                                                         |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.19x