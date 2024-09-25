# Results vs. 3.13.0b1

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 646 ms: 1.46x slower                                                 |
| docutils       | 3.94 sec                                                              | 5.06 sec: 1.28x slower                                               |
| html5lib       | 92.0 ms                                                               | 140 ms: 1.52x slower                                                 |
| tornado_http   | 253 ms                                                                | 367 ms: 1.45x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.43x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.15 sec: 1.25x faster                                               |
| async_tree_io              | 1.39 sec                                                              | 1.25 sec: 1.11x faster                                               |
| async_tree_none_tg         | 526 ms                                                                | 491 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 824 ms: 1.06x faster                                                 |
| asyncio_websockets         | 728 ms                                                                | 753 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 933 ms: 1.04x slower                                                 |
| async_tree_none            | 523 ms                                                                | 585 ms: 1.12x slower                                                 |
| asyncio_tcp                | 972 ms                                                                | 1.12 sec: 1.15x slower                                               |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.36 sec: 1.19x slower                                               |
| async_generators           | 588 ms                                                                | 753 ms: 1.28x slower                                                 |
| coroutines                 | 29.3 ms                                                               | 42.1 ms: 1.43x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                                         |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 256 ms                                                                | 242 ms: 1.06x faster                                                 |
| float          | 115 ms                                                                | 196 ms: 1.70x slower                                                 |
| nbody          | 126 ms                                                                | 284 ms: 2.26x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.54x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.63 ms                                                               | 4.82 ms: 1.04x slower                                                |
| regex_v8       | 37.1 ms                                                               | 39.2 ms: 1.06x slower                                                |
| regex_dna      | 284 ms                                                                | 301 ms: 1.06x slower                                                 |
| regex_compile  | 189 ms                                                                | 295 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.91 us: 1.08x faster                                                |
| pickle               | 15.2 us                                                               | 14.1 us: 1.08x faster                                                |
| pickle_dict          | 46.5 us                                                               | 43.9 us: 1.06x faster                                                |
| xml_etree_parse      | 216 ms                                                                | 232 ms: 1.07x slower                                                 |
| xml_etree_iterparse  | 163 ms                                                                | 179 ms: 1.10x slower                                                 |
| unpickle_list        | 6.78 us                                                               | 7.94 us: 1.17x slower                                                |
| json_loads           | 37.9 us                                                               | 45.4 us: 1.20x slower                                                |
| json_dumps           | 13.9 ms                                                               | 17.7 ms: 1.27x slower                                                |
| xml_etree_generate   | 120 ms                                                                | 164 ms: 1.37x slower                                                 |
| tomli_loads          | 2.84 sec                                                              | 4.20 sec: 1.48x slower                                               |
| xml_etree_process    | 82.2 ms                                                               | 135 ms: 1.64x slower                                                 |
| pickle_pure_python   | 428 us                                                                | 778 us: 1.82x slower                                                 |
| unpickle_pure_python | 285 us                                                                | 567 us: 1.99x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                                         |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 29.3 ms: 1.25x slower                                                |
| python_startup_no_site | 16.0 ms                                                               | 20.7 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.27x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 118 ms: 1.64x slower                                                 |
| django_template | 46.1 ms                                                               | 77.1 ms: 1.67x slower                                                |
| genshi_text     | 31.6 ms                                                               | 54.2 ms: 1.71x slower                                                |
| mako            | 16.7 ms                                                               | 32.1 ms: 1.93x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.73x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 13.8 ms: 16.59x faster                                               |
| create_gc_cycles           | 2.49 ms                                                               | 1.92 ms: 1.29x faster                                                |
| gc_traversal               | 5.80 ms                                                               | 4.63 ms: 1.25x faster                                                |
| async_tree_io_tg           | 1.43 sec                                                              | 1.15 sec: 1.25x faster                                               |
| bench_mp_pool              | 19.7 ms                                                               | 16.8 ms: 1.18x faster                                                |
| async_tree_io              | 1.39 sec                                                              | 1.25 sec: 1.11x faster                                               |
| pickle_list                | 7.48 us                                                               | 6.91 us: 1.08x faster                                                |
| pickle                     | 15.2 us                                                               | 14.1 us: 1.08x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 491 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 824 ms: 1.06x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 43.9 us: 1.06x faster                                                |
| pidigits                   | 256 ms                                                                | 242 ms: 1.06x faster                                                 |
| asyncio_websockets         | 728 ms                                                                | 753 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 933 ms: 1.04x slower                                                 |
| regex_effbot               | 4.63 ms                                                               | 4.82 ms: 1.04x slower                                                |
| regex_v8                   | 37.1 ms                                                               | 39.2 ms: 1.06x slower                                                |
| regex_dna                  | 284 ms                                                                | 301 ms: 1.06x slower                                                 |
| xml_etree_parse            | 216 ms                                                                | 232 ms: 1.07x slower                                                 |
| xml_etree_iterparse        | 163 ms                                                                | 179 ms: 1.10x slower                                                 |
| deepcopy                   | 498 us                                                                | 556 us: 1.12x slower                                                 |
| async_tree_none            | 523 ms                                                                | 585 ms: 1.12x slower                                                 |
| pathlib                    | 31.8 ms                                                               | 35.6 ms: 1.12x slower                                                |
| sqlite_synth               | 3.94 us                                                               | 4.44 us: 1.13x slower                                                |
| asyncio_tcp                | 972 ms                                                                | 1.12 sec: 1.15x slower                                               |
| unpickle_list              | 6.78 us                                                               | 7.94 us: 1.17x slower                                                |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.36 sec: 1.19x slower                                               |
| json_loads                 | 37.9 us                                                               | 45.4 us: 1.20x slower                                                |
| coverage                   | 121 ms                                                                | 146 ms: 1.21x slower                                                 |
| json                       | 6.79 ms                                                               | 8.22 ms: 1.21x slower                                                |
| meteor_contest             | 156 ms                                                                | 194 ms: 1.24x slower                                                 |
| python_startup             | 23.5 ms                                                               | 29.3 ms: 1.25x slower                                                |
| pylint                     | 466 ms                                                                | 590 ms: 1.27x slower                                                 |
| json_dumps                 | 13.9 ms                                                               | 17.7 ms: 1.27x slower                                                |
| async_generators           | 588 ms                                                                | 753 ms: 1.28x slower                                                 |
| docutils                   | 3.94 sec                                                              | 5.06 sec: 1.28x slower                                               |
| mdp                        | 4.01 sec                                                              | 5.16 sec: 1.29x slower                                               |
| python_startup_no_site     | 16.0 ms                                                               | 20.7 ms: 1.30x slower                                                |
| pycparser                  | 1.71 sec                                                              | 2.29 sec: 1.34x slower                                               |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 9.23 ms: 1.35x slower                                                |
| scimark_fft                | 469 ms                                                                | 635 ms: 1.35x slower                                                 |
| deepcopy_reduce            | 4.31 us                                                               | 5.84 us: 1.35x slower                                                |
| xml_etree_generate         | 120 ms                                                                | 164 ms: 1.37x slower                                                 |
| deepcopy_memo              | 50.9 us                                                               | 69.7 us: 1.37x slower                                                |
| generators                 | 40.7 ms                                                               | 57.5 ms: 1.41x slower                                                |
| coroutines                 | 29.3 ms                                                               | 42.1 ms: 1.43x slower                                                |
| bench_thread_pool          | 3.01 ms                                                               | 4.33 ms: 1.44x slower                                                |
| fannkuch                   | 535 ms                                                                | 776 ms: 1.45x slower                                                 |
| tornado_http               | 253 ms                                                                | 367 ms: 1.45x slower                                                 |
| 2to3                       | 441 ms                                                                | 646 ms: 1.46x slower                                                 |
| tomli_loads                | 2.84 sec                                                              | 4.20 sec: 1.48x slower                                               |
| nqueens                    | 108 ms                                                                | 161 ms: 1.48x slower                                                 |
| crypto_pyaes               | 102 ms                                                                | 152 ms: 1.50x slower                                                 |
| html5lib                   | 92.0 ms                                                               | 140 ms: 1.52x slower                                                 |
| pyflate                    | 710 ms                                                                | 1.09 sec: 1.53x slower                                               |
| sympy_integrate            | 28.7 ms                                                               | 44.3 ms: 1.54x slower                                                |
| regex_compile              | 189 ms                                                                | 295 ms: 1.55x slower                                                 |
| bpe_tokeniser              | 6.53 sec                                                              | 10.3 sec: 1.57x slower                                               |
| richards                   | 68.8 ms                                                               | 110 ms: 1.60x slower                                                 |
| typing_runtime_protocols   | 222 us                                                                | 356 us: 1.60x slower                                                 |
| sqlglot_normalize          | 150 ms                                                                | 242 ms: 1.61x slower                                                 |
| thrift                     | 1.09 ms                                                               | 1.77 ms: 1.63x slower                                                |
| genshi_xml                 | 71.9 ms                                                               | 118 ms: 1.64x slower                                                 |
| xml_etree_process          | 82.2 ms                                                               | 135 ms: 1.64x slower                                                 |
| logging_simple             | 9.16 us                                                               | 15.0 us: 1.64x slower                                                |
| pprint_safe_repr           | 991 ms                                                                | 1.64 sec: 1.66x slower                                               |
| django_template            | 46.1 ms                                                               | 77.1 ms: 1.67x slower                                                |
| spectral_norm              | 151 ms                                                                | 253 ms: 1.67x slower                                                 |
| richards_super             | 73.5 ms                                                               | 124 ms: 1.69x slower                                                 |
| comprehensions             | 22.6 us                                                               | 38.3 us: 1.69x slower                                                |
| pprint_pformat             | 2.04 sec                                                              | 3.45 sec: 1.69x slower                                               |
| float                      | 115 ms                                                                | 196 ms: 1.70x slower                                                 |
| genshi_text                | 31.6 ms                                                               | 54.2 ms: 1.71x slower                                                |
| sympy_str                  | 376 ms                                                                | 673 ms: 1.79x slower                                                 |
| scimark_monte_carlo        | 89.0 ms                                                               | 160 ms: 1.80x slower                                                 |
| pickle_pure_python         | 428 us                                                                | 778 us: 1.82x slower                                                 |
| sqlglot_optimize           | 77.9 ms                                                               | 143 ms: 1.84x slower                                                 |
| logging_silent             | 137 ns                                                                | 254 ns: 1.86x slower                                                 |
| mako                       | 16.7 ms                                                               | 32.1 ms: 1.93x slower                                                |
| scimark_sor                | 176 ms                                                                | 342 ms: 1.94x slower                                                 |
| sympy_expand               | 638 ms                                                                | 1.26 sec: 1.98x slower                                               |
| logging_format             | 9.36 us                                                               | 18.5 us: 1.98x slower                                                |
| unpickle_pure_python       | 285 us                                                                | 567 us: 1.99x slower                                                 |
| scimark_lu                 | 150 ms                                                                | 303 ms: 2.02x slower                                                 |
| hexiom                     | 8.42 ms                                                               | 17.2 ms: 2.04x slower                                                |
| sympy_sum                  | 226 ms                                                                | 465 ms: 2.06x slower                                                 |
| sqlglot_transpile          | 2.24 ms                                                               | 4.62 ms: 2.06x slower                                                |
| chaos                      | 81.5 ms                                                               | 169 ms: 2.07x slower                                                 |
| raytrace                   | 351 ms                                                                | 765 ms: 2.18x slower                                                 |
| nbody                      | 126 ms                                                                | 284 ms: 2.26x slower                                                 |
| go                         | 193 ms                                                                | 446 ms: 2.31x slower                                                 |
| sqlglot_parse              | 1.92 ms                                                               | 4.43 ms: 2.31x slower                                                |
| deltablue                  | 4.55 ms                                                               | 11.3 ms: 2.50x slower                                                |
| unpack_sequence            | 54.6 ns                                                               | 211 ns: 3.86x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.37x slower                                                         |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, unpickle
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x