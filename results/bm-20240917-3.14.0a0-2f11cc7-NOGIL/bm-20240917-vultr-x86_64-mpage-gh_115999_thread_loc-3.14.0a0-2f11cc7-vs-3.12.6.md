# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: 2f11cc7
- commit date: 2024-09-17
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 414 ms: 1.57x slower                                                 |
| docutils       | 2.64 sec                                               | 3.34 sec: 1.27x slower                                               |
| html5lib       | 63.6 ms                                                | 103 ms: 1.62x slower                                                 |
| tornado_http   | 119 ms                                                 | 162 ms: 1.36x slower                                                 |
| Geometric mean | (ref)                                                  | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 909 ms: 1.22x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 475 ms: 1.18x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 379 ms: 1.18x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 941 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 639 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 420 ms: 1.11x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 510 ms: 1.09x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 673 ms: 1.06x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.83 sec: 1.21x slower                                               |
| coroutines                 | 23.9 ms                                                | 29.8 ms: 1.24x slower                                                |
| async_generators           | 384 ms                                                 | 493 ms: 1.28x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| float          | 80.8 ms                                                | 148 ms: 1.83x slower                                                 |
| nbody          | 89.3 ms                                                | 185 ms: 2.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.56x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.36 ms: 1.06x slower                                                |
| regex_dna      | 168 ms                                                 | 196 ms: 1.17x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                |
| regex_compile  | 142 ms                                                 | 223 ms: 1.57x slower                                                 |
| Geometric mean | (ref)                                                  | 1.25x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 135 ms: 1.03x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.01x faster                                                |
| pickle               | 10.9 us                                                | 11.1 us: 1.01x slower                                                |
| pickle_list          | 4.77 us                                                | 4.85 us: 1.02x slower                                                |
| unpickle             | 14.1 us                                                | 15.2 us: 1.08x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.05 us: 1.08x slower                                                |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 107 ms: 1.11x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 112 ms: 1.32x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.7 ms: 1.32x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.17 sec: 1.51x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 91.8 ms: 1.56x slower                                                |
| unpickle_pure_python | 221 us                                                 | 412 us: 1.87x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 604 us: 1.96x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.24x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 80.9 ms: 1.61x slower                                                |
| genshi_text     | 22.8 ms                                                | 39.8 ms: 1.75x slower                                                |
| django_template | 34.7 ms                                                | 63.5 ms: 1.83x slower                                                |
| mako            | 11.0 ms                                                | 20.3 ms: 1.85x slower                                                |
| Geometric mean  | (ref)                                                  | 1.76x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 2.45 ms: 1.41x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 909 ms: 1.22x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 475 ms: 1.18x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 379 ms: 1.18x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 941 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 639 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 420 ms: 1.11x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 510 ms: 1.09x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 673 ms: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 135 ms: 1.03x faster                                                 |
| pidigits                   | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| pickle_dict                | 31.8 us                                                | 31.6 us: 1.01x faster                                                |
| pickle                     | 10.9 us                                                | 11.1 us: 1.01x slower                                                |
| pickle_list                | 4.77 us                                                | 4.85 us: 1.02x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.11 ms: 1.02x slower                                                |
| json                       | 5.02 ms                                                | 5.31 ms: 1.06x slower                                                |
| regex_effbot               | 3.17 ms                                                | 3.36 ms: 1.06x slower                                                |
| unpickle                   | 14.1 us                                                | 15.2 us: 1.08x slower                                                |
| unpickle_list              | 4.67 us                                                | 5.05 us: 1.08x slower                                                |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.40 us: 1.09x slower                                                |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 107 ms: 1.11x slower                                                 |
| scimark_fft                | 342 ms                                                 | 386 ms: 1.13x slower                                                 |
| regex_dna                  | 168 ms                                                 | 196 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.21 ms: 1.19x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.83 sec: 1.21x slower                                               |
| deepcopy                   | 352 us                                                 | 435 us: 1.24x slower                                                 |
| coroutines                 | 23.9 ms                                                | 29.8 ms: 1.24x slower                                                |
| regex_v8                   | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                |
| docutils                   | 2.64 sec                                               | 3.34 sec: 1.27x slower                                               |
| async_generators           | 384 ms                                                 | 493 ms: 1.28x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 102 ms: 1.29x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 6.12 sec: 1.29x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 14.0 ms: 1.29x slower                                                |
| generators                 | 32.2 ms                                                | 42.0 ms: 1.30x slower                                                |
| mdp                        | 2.42 sec                                               | 3.17 sec: 1.31x slower                                               |
| xml_etree_generate         | 85.2 ms                                                | 112 ms: 1.32x slower                                                 |
| pylint                     | 319 ms                                                 | 420 ms: 1.32x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.7 ms: 1.32x slower                                                |
| spectral_norm              | 110 ms                                                 | 146 ms: 1.32x slower                                                 |
| meteor_contest             | 104 ms                                                 | 138 ms: 1.33x slower                                                 |
| tornado_http               | 119 ms                                                 | 162 ms: 1.36x slower                                                 |
| deepcopy_memo              | 40.3 us                                                | 56.0 us: 1.39x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 107 ms: 1.39x slower                                                 |
| nqueens                    | 80.1 ms                                                | 114 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| coverage                   | 71.4 ms                                                | 103 ms: 1.44x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.69 sec: 1.44x slower                                               |
| telco                      | 6.53 ms                                                | 9.57 ms: 1.47x slower                                                |
| deepcopy_reduce            | 3.08 us                                                | 4.54 us: 1.48x slower                                                |
| fannkuch                   | 372 ms                                                 | 551 ms: 1.48x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 245 us: 1.50x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 3.17 sec: 1.51x slower                                               |
| comprehensions             | 19.8 us                                                | 29.9 us: 1.51x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 91.8 ms: 1.56x slower                                                |
| regex_compile              | 142 ms                                                 | 223 ms: 1.57x slower                                                 |
| 2to3                       | 264 ms                                                 | 414 ms: 1.57x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 32.5 ms: 1.58x slower                                                |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| thrift                     | 791 us                                                 | 1.27 ms: 1.60x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 80.9 ms: 1.61x slower                                                |
| html5lib                   | 63.6 ms                                                | 103 ms: 1.62x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 179 ms: 1.68x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 90.0 ms: 1.69x slower                                                |
| pyflate                    | 448 ms                                                 | 769 ms: 1.72x slower                                                 |
| genshi_text                | 22.8 ms                                                | 39.8 ms: 1.75x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 1.32 sec: 1.77x slower                                               |
| scimark_monte_carlo        | 68.4 ms                                                | 122 ms: 1.79x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 2.74 sec: 1.80x slower                                               |
| logging_format             | 7.35 us                                                | 13.4 us: 1.83x slower                                                |
| django_template            | 34.7 ms                                                | 63.5 ms: 1.83x slower                                                |
| float                      | 80.8 ms                                                | 148 ms: 1.83x slower                                                 |
| sympy_str                  | 292 ms                                                 | 535 ms: 1.84x slower                                                 |
| logging_simple             | 6.63 us                                                | 12.2 us: 1.84x slower                                                |
| mako                       | 11.0 ms                                                | 20.3 ms: 1.85x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 412 us: 1.87x slower                                                 |
| chaos                      | 62.8 ms                                                | 118 ms: 1.87x slower                                                 |
| richards                   | 45.9 ms                                                | 89.1 ms: 1.94x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 3.28 ms: 1.96x slower                                                |
| pickle_pure_python         | 308 us                                                 | 604 us: 1.96x slower                                                 |
| hexiom                     | 6.17 ms                                                | 12.1 ms: 1.97x slower                                                |
| scimark_sor                | 130 ms                                                 | 256 ms: 1.97x slower                                                 |
| logging_silent             | 109 ns                                                 | 218 ns: 2.00x slower                                                 |
| richards_super             | 51.9 ms                                                | 107 ms: 2.06x slower                                                 |
| nbody                      | 89.3 ms                                                | 185 ms: 2.07x slower                                                 |
| raytrace                   | 299 ms                                                 | 626 ms: 2.09x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 240 ms: 2.10x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.85 ms: 2.10x slower                                                |
| go                         | 139 ms                                                 | 294 ms: 2.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 1.05 sec: 2.24x slower                                               |
| sympy_sum                  | 166 ms                                                 | 380 ms: 2.29x slower                                                 |
| unpack_sequence            | 52.1 ns                                                | 133 ns: 2.56x slower                                                 |
| deltablue                  | 3.45 ms                                                | 9.04 ms: 2.62x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.18 ms: 3.38x slower                                                |
| Geometric mean             | (ref)                                                  | 1.42x slower                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, pathlib
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.20x