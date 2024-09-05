# Results vs. 3.13.0b1

- fork: mpage
- ref: gh_115999_measure_sp
- machine: linux-x86_64
- commit hash: aa5b4de
- commit date: 2024-09-04
- overall geometric mean: 1.19x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 526 ms: 1.19x slower                                                 |
| docutils       | 3.94 sec                                                              | 4.57 sec: 1.16x slower                                               |
| html5lib       | 92.0 ms                                                               | 128 ms: 1.39x slower                                                 |
| tornado_http   | 253 ms                                                                | 279 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.21x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets         | 728 ms                                                                | 751 ms: 1.03x slower                                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 2.93 sec: 1.04x slower                                               |
| async_tree_memoization     | 775 ms                                                                | 822 ms: 1.06x slower                                                 |
| async_generators           | 588 ms                                                                | 624 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 983 ms: 1.09x slower                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.62 sec: 1.13x slower                                               |
| async_tree_io              | 1.39 sec                                                              | 1.58 sec: 1.14x slower                                               |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 1.03 sec: 1.18x slower                                               |
| async_tree_none_tg         | 526 ms                                                                | 620 ms: 1.18x slower                                                 |
| async_tree_memoization_tg  | 692 ms                                                                | 827 ms: 1.20x slower                                                 |
| async_tree_none            | 523 ms                                                                | 656 ms: 1.25x slower                                                 |
| coroutines                 | 29.3 ms                                                               | 40.5 ms: 1.38x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.13x slower                                                         |

Benchmark hidden because not significant (1): asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 115 ms                                                                | 169 ms: 1.47x slower                                                 |
| nbody          | 126 ms                                                                | 191 ms: 1.52x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.32x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 296 ms: 1.05x slower                                                 |
| regex_effbot   | 4.63 ms                                                               | 5.30 ms: 1.14x slower                                                |
| regex_compile  | 189 ms                                                                | 252 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 22.2 us                                                               | 19.3 us: 1.15x faster                                                |
| pickle_list          | 7.48 us                                                               | 6.97 us: 1.07x faster                                                |
| unpickle_list        | 6.78 us                                                               | 7.01 us: 1.03x slower                                                |
| pickle               | 15.2 us                                                               | 16.0 us: 1.05x slower                                                |
| json_loads           | 37.9 us                                                               | 40.2 us: 1.06x slower                                                |
| xml_etree_parse      | 216 ms                                                                | 235 ms: 1.08x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 148 ms: 1.23x slower                                                 |
| tomli_loads          | 2.84 sec                                                              | 3.60 sec: 1.27x slower                                               |
| json_dumps           | 13.9 ms                                                               | 17.8 ms: 1.28x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 110 ms: 1.34x slower                                                 |
| unpickle_pure_python | 285 us                                                                | 434 us: 1.52x slower                                                 |
| pickle_pure_python   | 428 us                                                                | 755 us: 1.77x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.16x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 94.1 ms: 1.31x slower                                                |
| genshi_text     | 31.6 ms                                                               | 43.1 ms: 1.36x slower                                                |
| django_template | 46.1 ms                                                               | 65.8 ms: 1.43x slower                                                |
| mako            | 16.7 ms                                                               | 24.1 ms: 1.45x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.39x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 11.4 ms: 20.16x faster                                               |
| unpickle                   | 22.2 us                                                               | 19.3 us: 1.15x faster                                                |
| coverage                   | 121 ms                                                                | 112 ms: 1.07x faster                                                 |
| pickle_list                | 7.48 us                                                               | 6.97 us: 1.07x faster                                                |
| asyncio_websockets         | 728 ms                                                                | 751 ms: 1.03x slower                                                 |
| unpickle_list              | 6.78 us                                                               | 7.01 us: 1.03x slower                                                |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 2.93 sec: 1.04x slower                                               |
| regex_dna                  | 284 ms                                                                | 296 ms: 1.05x slower                                                 |
| pickle                     | 15.2 us                                                               | 16.0 us: 1.05x slower                                                |
| async_tree_memoization     | 775 ms                                                                | 822 ms: 1.06x slower                                                 |
| async_generators           | 588 ms                                                                | 624 ms: 1.06x slower                                                 |
| json_loads                 | 37.9 us                                                               | 40.2 us: 1.06x slower                                                |
| create_gc_cycles           | 2.49 ms                                                               | 2.65 ms: 1.07x slower                                                |
| xml_etree_parse            | 216 ms                                                                | 235 ms: 1.08x slower                                                 |
| sympy_sum                  | 226 ms                                                                | 246 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 7.48 ms: 1.09x slower                                                |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 983 ms: 1.09x slower                                                 |
| tornado_http               | 253 ms                                                                | 279 ms: 1.10x slower                                                 |
| sympy_str                  | 376 ms                                                                | 423 ms: 1.12x slower                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.62 sec: 1.13x slower                                               |
| async_tree_io              | 1.39 sec                                                              | 1.58 sec: 1.14x slower                                               |
| sympy_expand               | 638 ms                                                                | 729 ms: 1.14x slower                                                 |
| regex_effbot               | 4.63 ms                                                               | 5.30 ms: 1.14x slower                                                |
| nqueens                    | 108 ms                                                                | 125 ms: 1.15x slower                                                 |
| docutils                   | 3.94 sec                                                              | 4.57 sec: 1.16x slower                                               |
| pylint                     | 466 ms                                                                | 542 ms: 1.16x slower                                                 |
| deepcopy_reduce            | 4.31 us                                                               | 5.02 us: 1.17x slower                                                |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 1.03 sec: 1.18x slower                                               |
| async_tree_none_tg         | 526 ms                                                                | 620 ms: 1.18x slower                                                 |
| generators                 | 40.7 ms                                                               | 48.0 ms: 1.18x slower                                                |
| scimark_fft                | 469 ms                                                                | 555 ms: 1.18x slower                                                 |
| sympy_integrate            | 28.7 ms                                                               | 34.0 ms: 1.18x slower                                                |
| bpe_tokeniser              | 6.53 sec                                                              | 7.74 sec: 1.18x slower                                               |
| deepcopy_memo              | 50.9 us                                                               | 60.6 us: 1.19x slower                                                |
| 2to3                       | 441 ms                                                                | 526 ms: 1.19x slower                                                 |
| async_tree_memoization_tg  | 692 ms                                                                | 827 ms: 1.20x slower                                                 |
| unpack_sequence            | 54.6 ns                                                               | 65.7 ns: 1.20x slower                                                |
| bench_thread_pool          | 3.01 ms                                                               | 3.64 ms: 1.21x slower                                                |
| pycparser                  | 1.71 sec                                                              | 2.07 sec: 1.21x slower                                               |
| typing_runtime_protocols   | 222 us                                                                | 269 us: 1.21x slower                                                 |
| richards                   | 68.8 ms                                                               | 84.3 ms: 1.22x slower                                                |
| xml_etree_generate         | 120 ms                                                                | 148 ms: 1.23x slower                                                 |
| crypto_pyaes               | 102 ms                                                                | 126 ms: 1.24x slower                                                 |
| thrift                     | 1.09 ms                                                               | 1.35 ms: 1.25x slower                                                |
| fannkuch                   | 535 ms                                                                | 670 ms: 1.25x slower                                                 |
| async_tree_none            | 523 ms                                                                | 656 ms: 1.25x slower                                                 |
| json                       | 6.79 ms                                                               | 8.58 ms: 1.26x slower                                                |
| tomli_loads                | 2.84 sec                                                              | 3.60 sec: 1.27x slower                                               |
| json_dumps                 | 13.9 ms                                                               | 17.8 ms: 1.28x slower                                                |
| sqlglot_optimize           | 77.9 ms                                                               | 99.9 ms: 1.28x slower                                                |
| sqlglot_normalize          | 150 ms                                                                | 196 ms: 1.31x slower                                                 |
| spectral_norm              | 151 ms                                                                | 198 ms: 1.31x slower                                                 |
| genshi_xml                 | 71.9 ms                                                               | 94.1 ms: 1.31x slower                                                |
| pyflate                    | 710 ms                                                                | 934 ms: 1.31x slower                                                 |
| pprint_pformat             | 2.04 sec                                                              | 2.69 sec: 1.32x slower                                               |
| regex_compile              | 189 ms                                                                | 252 ms: 1.33x slower                                                 |
| xml_etree_process          | 82.2 ms                                                               | 110 ms: 1.34x slower                                                 |
| bench_mp_pool              | 19.7 ms                                                               | 26.3 ms: 1.34x slower                                                |
| genshi_text                | 31.6 ms                                                               | 43.1 ms: 1.36x slower                                                |
| pprint_safe_repr           | 991 ms                                                                | 1.36 sec: 1.37x slower                                               |
| coroutines                 | 29.3 ms                                                               | 40.5 ms: 1.38x slower                                                |
| comprehensions             | 22.6 us                                                               | 31.3 us: 1.38x slower                                                |
| html5lib                   | 92.0 ms                                                               | 128 ms: 1.39x slower                                                 |
| django_template            | 46.1 ms                                                               | 65.8 ms: 1.43x slower                                                |
| mako                       | 16.7 ms                                                               | 24.1 ms: 1.45x slower                                                |
| logging_simple             | 9.16 us                                                               | 13.3 us: 1.45x slower                                                |
| float                      | 115 ms                                                                | 169 ms: 1.47x slower                                                 |
| sqlglot_parse              | 1.92 ms                                                               | 2.87 ms: 1.49x slower                                                |
| scimark_monte_carlo        | 89.0 ms                                                               | 134 ms: 1.50x slower                                                 |
| go                         | 193 ms                                                                | 291 ms: 1.51x slower                                                 |
| unpickle_pure_python       | 285 us                                                                | 434 us: 1.52x slower                                                 |
| nbody                      | 126 ms                                                                | 191 ms: 1.52x slower                                                 |
| logging_format             | 9.36 us                                                               | 14.8 us: 1.58x slower                                                |
| richards_super             | 73.5 ms                                                               | 117 ms: 1.59x slower                                                 |
| logging_silent             | 137 ns                                                                | 218 ns: 1.60x slower                                                 |
| sqlglot_transpile          | 2.24 ms                                                               | 3.62 ms: 1.61x slower                                                |
| chaos                      | 81.5 ms                                                               | 133 ms: 1.64x slower                                                 |
| scimark_sor                | 176 ms                                                                | 290 ms: 1.65x slower                                                 |
| raytrace                   | 351 ms                                                                | 605 ms: 1.72x slower                                                 |
| scimark_lu                 | 150 ms                                                                | 259 ms: 1.73x slower                                                 |
| pickle_pure_python         | 428 us                                                                | 755 us: 1.77x slower                                                 |
| hexiom                     | 8.42 ms                                                               | 15.0 ms: 1.78x slower                                                |
| deltablue                  | 4.55 ms                                                               | 9.49 ms: 2.09x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.19x slower                                                         |

Benchmark hidden because not significant (13): pathlib, regex_v8, python_startup_no_site, mdp, deepcopy, python_startup, meteor_contest, xml_etree_iterparse, asyncio_tcp, pickle_dict, pidigits, sqlite_synth, gc_traversal
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.00x