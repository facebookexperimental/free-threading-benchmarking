# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 661 ms: 1.50x slower                                  |
| docutils       | 4.01 sec                                                | 4.69 sec: 1.17x slower                                |
| html5lib       | 98.1 ms                                                 | 135 ms: 1.38x slower                                  |
| tornado_http   | 248 ms                                                  | 320 ms: 1.29x slower                                  |
| Geometric mean | (ref)                                                   | 1.33x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.15 sec: 1.27x faster                                |
| async_tree_io              | 1.38 sec                                                | 1.25 sec: 1.11x faster                                |
| async_tree_none_tg         | 521 ms                                                  | 479 ms: 1.09x faster                                  |
| asyncio_websockets         | 772 ms                                                  | 714 ms: 1.08x faster                                  |
| async_tree_memoization_tg  | 672 ms                                                  | 632 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 806 ms: 1.05x faster                                  |
| asyncio_tcp                | 985 ms                                                  | 1.05 sec: 1.06x slower                                |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.12 sec: 1.12x slower                                |
| async_generators           | 592 ms                                                  | 739 ms: 1.25x slower                                  |
| coroutines                 | 29.2 ms                                                 | 40.7 ms: 1.39x slower                                 |
| Geometric mean             | (ref)                                                   | 1.01x slower                                          |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 248 ms                                                  | 241 ms: 1.03x faster                                  |
| float          | 115 ms                                                  | 199 ms: 1.73x slower                                  |
| nbody          | 124 ms                                                  | 284 ms: 2.29x slower                                  |
| Geometric mean | (ref)                                                   | 1.57x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.60 ms: 1.05x faster                                 |
| regex_v8       | 32.4 ms                                                 | 35.5 ms: 1.09x slower                                 |
| regex_compile  | 177 ms                                                  | 287 ms: 1.62x slower                                  |
| Geometric mean | (ref)                                                   | 1.14x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_iterparse  | 176 ms                                                  | 152 ms: 1.16x faster                                  |
| xml_etree_parse      | 236 ms                                                  | 203 ms: 1.16x faster                                  |
| pickle_dict          | 46.5 us                                                 | 40.4 us: 1.15x faster                                 |
| pickle               | 15.4 us                                                 | 14.4 us: 1.07x faster                                 |
| pickle_list          | 6.82 us                                                 | 6.56 us: 1.04x faster                                 |
| unpickle_list        | 6.67 us                                                 | 7.37 us: 1.11x slower                                 |
| json_loads           | 36.1 us                                                 | 41.9 us: 1.16x slower                                 |
| json_dumps           | 14.9 ms                                                 | 18.2 ms: 1.22x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 160 ms: 1.24x slower                                  |
| xml_etree_process    | 86.5 ms                                                 | 119 ms: 1.37x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.17 sec: 1.49x slower                                |
| unpickle_pure_python | 296 us                                                  | 526 us: 1.78x slower                                  |
| pickle_pure_python   | 417 us                                                  | 792 us: 1.90x slower                                  |
| Geometric mean       | (ref)                                                   | 1.16x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 27.3 ms: 1.24x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 18.6 ms: 1.27x slower                                 |
| Geometric mean         | (ref)                                                   | 1.25x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 117 ms: 1.71x slower                                  |
| django_template | 46.9 ms                                                 | 80.7 ms: 1.72x slower                                 |
| genshi_text     | 31.7 ms                                                 | 54.8 ms: 1.73x slower                                 |
| mako            | 16.1 ms                                                 | 29.7 ms: 1.85x slower                                 |
| Geometric mean  | (ref)                                                   | 1.75x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool              | 19.4 ms                                                 | 12.0 ms: 1.61x faster                                 |
| gc_traversal               | 5.91 ms                                                 | 4.22 ms: 1.40x faster                                 |
| create_gc_cycles           | 2.46 ms                                                 | 1.77 ms: 1.39x faster                                 |
| async_tree_io_tg           | 1.46 sec                                                | 1.15 sec: 1.27x faster                                |
| xml_etree_iterparse        | 176 ms                                                  | 152 ms: 1.16x faster                                  |
| xml_etree_parse            | 236 ms                                                  | 203 ms: 1.16x faster                                  |
| pickle_dict                | 46.5 us                                                 | 40.4 us: 1.15x faster                                 |
| async_tree_io              | 1.38 sec                                                | 1.25 sec: 1.11x faster                                |
| async_tree_none_tg         | 521 ms                                                  | 479 ms: 1.09x faster                                  |
| asyncio_websockets         | 772 ms                                                  | 714 ms: 1.08x faster                                  |
| pickle                     | 15.4 us                                                 | 14.4 us: 1.07x faster                                 |
| async_tree_memoization_tg  | 672 ms                                                  | 632 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 806 ms: 1.05x faster                                  |
| regex_effbot               | 4.84 ms                                                 | 4.60 ms: 1.05x faster                                 |
| pickle_list                | 6.82 us                                                 | 6.56 us: 1.04x faster                                 |
| pidigits                   | 248 ms                                                  | 241 ms: 1.03x faster                                  |
| sqlite_synth               | 4.07 us                                                 | 4.31 us: 1.06x slower                                 |
| asyncio_tcp                | 985 ms                                                  | 1.05 sec: 1.06x slower                                |
| pathlib                    | 29.3 ms                                                 | 31.7 ms: 1.08x slower                                 |
| regex_v8                   | 32.4 ms                                                 | 35.5 ms: 1.09x slower                                 |
| unpickle_list              | 6.67 us                                                 | 7.37 us: 1.11x slower                                 |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.12 sec: 1.12x slower                                |
| telco                      | 11.4 ms                                                 | 13.2 ms: 1.16x slower                                 |
| json_loads                 | 36.1 us                                                 | 41.9 us: 1.16x slower                                 |
| docutils                   | 4.01 sec                                                | 4.69 sec: 1.17x slower                                |
| pylint                     | 472 ms                                                  | 554 ms: 1.17x slower                                  |
| bench_thread_pool          | 3.06 ms                                                 | 3.73 ms: 1.22x slower                                 |
| json_dumps                 | 14.9 ms                                                 | 18.2 ms: 1.22x slower                                 |
| json                       | 6.55 ms                                                 | 8.04 ms: 1.23x slower                                 |
| xml_etree_generate         | 129 ms                                                  | 160 ms: 1.24x slower                                  |
| python_startup             | 22.0 ms                                                 | 27.3 ms: 1.24x slower                                 |
| meteor_contest             | 157 ms                                                  | 196 ms: 1.25x slower                                  |
| async_generators           | 592 ms                                                  | 739 ms: 1.25x slower                                  |
| deepcopy                   | 484 us                                                  | 608 us: 1.26x slower                                  |
| python_startup_no_site     | 14.6 ms                                                 | 18.6 ms: 1.27x slower                                 |
| tornado_http               | 248 ms                                                  | 320 ms: 1.29x slower                                  |
| scimark_fft                | 477 ms                                                  | 616 ms: 1.29x slower                                  |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 9.03 ms: 1.29x slower                                 |
| mdp                        | 3.80 sec                                                | 5.07 sec: 1.34x slower                                |
| deepcopy_memo              | 51.7 us                                                 | 69.3 us: 1.34x slower                                 |
| generators                 | 39.2 ms                                                 | 52.7 ms: 1.35x slower                                 |
| dulwich_log                | 100.0 ms                                                | 135 ms: 1.35x slower                                  |
| coverage                   | 110 ms                                                  | 149 ms: 1.35x slower                                  |
| pycparser                  | 1.57 sec                                                | 2.15 sec: 1.37x slower                                |
| xml_etree_process          | 86.5 ms                                                 | 119 ms: 1.37x slower                                  |
| html5lib                   | 98.1 ms                                                 | 135 ms: 1.38x slower                                  |
| coroutines                 | 29.2 ms                                                 | 40.7 ms: 1.39x slower                                 |
| deepcopy_reduce            | 4.27 us                                                 | 6.01 us: 1.41x slower                                 |
| nqueens                    | 108 ms                                                  | 153 ms: 1.42x slower                                  |
| sympy_integrate            | 29.7 ms                                                 | 43.4 ms: 1.46x slower                                 |
| fannkuch                   | 543 ms                                                  | 794 ms: 1.46x slower                                  |
| tomli_loads                | 2.80 sec                                                | 4.17 sec: 1.49x slower                                |
| 2to3                       | 442 ms                                                  | 661 ms: 1.50x slower                                  |
| crypto_pyaes               | 99.8 ms                                                 | 150 ms: 1.50x slower                                  |
| richards                   | 65.8 ms                                                 | 99.0 ms: 1.50x slower                                 |
| spectral_norm              | 159 ms                                                  | 245 ms: 1.54x slower                                  |
| thrift                     | 1.11 ms                                                 | 1.71 ms: 1.54x slower                                 |
| bpe_tokeniser              | 6.25 sec                                                | 9.73 sec: 1.56x slower                                |
| typing_runtime_protocols   | 216 us                                                  | 337 us: 1.56x slower                                  |
| sqlglot_optimize           | 76.2 ms                                                 | 121 ms: 1.58x slower                                  |
| richards_super             | 76.3 ms                                                 | 122 ms: 1.60x slower                                  |
| sqlglot_normalize          | 146 ms                                                  | 235 ms: 1.61x slower                                  |
| regex_compile              | 177 ms                                                  | 287 ms: 1.62x slower                                  |
| pyflate                    | 661 ms                                                  | 1.08 sec: 1.63x slower                                |
| genshi_xml                 | 68.3 ms                                                 | 117 ms: 1.71x slower                                  |
| django_template            | 46.9 ms                                                 | 80.7 ms: 1.72x slower                                 |
| genshi_text                | 31.7 ms                                                 | 54.8 ms: 1.73x slower                                 |
| logging_simple             | 8.98 us                                                 | 15.5 us: 1.73x slower                                 |
| float                      | 115 ms                                                  | 199 ms: 1.73x slower                                  |
| pprint_pformat             | 2.00 sec                                                | 3.50 sec: 1.75x slower                                |
| logging_format             | 9.48 us                                                 | 16.8 us: 1.78x slower                                 |
| unpickle_pure_python       | 296 us                                                  | 526 us: 1.78x slower                                  |
| pprint_safe_repr           | 959 ms                                                  | 1.71 sec: 1.78x slower                                |
| sympy_str                  | 367 ms                                                  | 664 ms: 1.81x slower                                  |
| scimark_monte_carlo        | 89.9 ms                                                 | 165 ms: 1.83x slower                                  |
| logging_silent             | 130 ns                                                  | 240 ns: 1.85x slower                                  |
| mako                       | 16.1 ms                                                 | 29.7 ms: 1.85x slower                                 |
| sqlglot_transpile          | 2.30 ms                                                 | 4.33 ms: 1.88x slower                                 |
| pickle_pure_python         | 417 us                                                  | 792 us: 1.90x slower                                  |
| chaos                      | 84.7 ms                                                 | 165 ms: 1.95x slower                                  |
| scimark_sor                | 172 ms                                                  | 337 ms: 1.96x slower                                  |
| hexiom                     | 8.35 ms                                                 | 16.5 ms: 1.97x slower                                 |
| sympy_expand               | 631 ms                                                  | 1.27 sec: 2.01x slower                                |
| comprehensions             | 20.9 us                                                 | 42.1 us: 2.01x slower                                 |
| go                         | 195 ms                                                  | 395 ms: 2.02x slower                                  |
| sqlglot_parse              | 1.80 ms                                                 | 3.77 ms: 2.10x slower                                 |
| scimark_lu                 | 154 ms                                                  | 326 ms: 2.12x slower                                  |
| sympy_sum                  | 213 ms                                                  | 460 ms: 2.16x slower                                  |
| raytrace                   | 350 ms                                                  | 784 ms: 2.24x slower                                  |
| nbody                      | 124 ms                                                  | 284 ms: 2.29x slower                                  |
| deltablue                  | 4.56 ms                                                 | 10.8 ms: 2.37x slower                                 |
| unpack_sequence            | 73.9 ns                                                 | 191 ns: 2.58x slower                                  |
| Geometric mean             | (ref)                                                   | 1.36x slower                                          |

Benchmark hidden because not significant (5): async_tree_memoization, regex_dna, unpickle, async_tree_none, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.15x