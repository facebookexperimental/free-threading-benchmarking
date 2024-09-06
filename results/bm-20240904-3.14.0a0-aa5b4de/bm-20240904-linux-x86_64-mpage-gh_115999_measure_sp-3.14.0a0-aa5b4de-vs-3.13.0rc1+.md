# Results vs. 3.13.0rc1+

- fork: mpage
- ref: gh_115999_measure_sp
- machine: linux-x86_64
- commit hash: aa5b4de
- commit date: 2024-09-04
- overall geometric mean: 1.23x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 526 ms: 1.19x slower                                                 |
| docutils       | 4.01 sec                                                | 4.57 sec: 1.14x slower                                               |
| html5lib       | 98.1 ms                                                 | 128 ms: 1.30x slower                                                 |
| tornado_http   | 248 ms                                                  | 279 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                   | 1.19x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets         | 772 ms                                                  | 751 ms: 1.03x faster                                                 |
| asyncio_tcp_ssl            | 2.79 sec                                                | 2.93 sec: 1.05x slower                                               |
| async_generators           | 592 ms                                                  | 624 ms: 1.05x slower                                                 |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 983 ms: 1.09x slower                                                 |
| async_tree_memoization     | 745 ms                                                  | 822 ms: 1.10x slower                                                 |
| async_tree_io_tg           | 1.46 sec                                                | 1.62 sec: 1.12x slower                                               |
| async_tree_none            | 576 ms                                                  | 656 ms: 1.14x slower                                                 |
| async_tree_io              | 1.38 sec                                                | 1.58 sec: 1.15x slower                                               |
| async_tree_none_tg         | 521 ms                                                  | 620 ms: 1.19x slower                                                 |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 1.03 sec: 1.22x slower                                               |
| async_tree_memoization_tg  | 672 ms                                                  | 827 ms: 1.23x slower                                                 |
| coroutines                 | 29.2 ms                                                 | 40.5 ms: 1.39x slower                                                |
| Geometric mean             | (ref)                                                   | 1.13x slower                                                         |

Benchmark hidden because not significant (1): asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 248 ms                                                  | 266 ms: 1.08x slower                                                 |
| float          | 115 ms                                                  | 169 ms: 1.47x slower                                                 |
| nbody          | 124 ms                                                  | 191 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                   | 1.35x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 5.30 ms: 1.09x slower                                                |
| regex_v8       | 32.4 ms                                                 | 36.1 ms: 1.11x slower                                                |
| regex_compile  | 177 ms                                                  | 252 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                   | 1.16x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 21.4 us                                                 | 19.3 us: 1.10x faster                                                |
| unpickle_list        | 6.67 us                                                 | 7.01 us: 1.05x slower                                                |
| json_loads           | 36.1 us                                                 | 40.2 us: 1.11x slower                                                |
| xml_etree_generate   | 129 ms                                                  | 148 ms: 1.14x slower                                                 |
| json_dumps           | 14.9 ms                                                 | 17.8 ms: 1.20x slower                                                |
| xml_etree_process    | 86.5 ms                                                 | 110 ms: 1.27x slower                                                 |
| tomli_loads          | 2.80 sec                                                | 3.60 sec: 1.29x slower                                               |
| unpickle_pure_python | 296 us                                                  | 434 us: 1.47x slower                                                 |
| pickle_pure_python   | 417 us                                                  | 755 us: 1.81x slower                                                 |
| Geometric mean       | (ref)                                                   | 1.14x slower                                                         |

Benchmark hidden because not significant (5): xml_etree_iterparse, xml_etree_parse, pickle_list, pickle_dict, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 23.4 ms: 1.06x slower                                                |
| python_startup_no_site | 14.6 ms                                                 | 15.8 ms: 1.08x slower                                                |
| Geometric mean         | (ref)                                                   | 1.07x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 43.1 ms: 1.36x slower                                                |
| genshi_xml      | 68.3 ms                                                 | 94.1 ms: 1.38x slower                                                |
| django_template | 46.9 ms                                                 | 65.8 ms: 1.40x slower                                                |
| mako            | 16.1 ms                                                 | 24.1 ms: 1.50x slower                                                |
| Geometric mean  | (ref)                                                   | 1.41x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpack_sequence            | 73.9 ns                                                 | 65.7 ns: 1.13x faster                                                |
| unpickle                   | 21.4 us                                                 | 19.3 us: 1.10x faster                                                |
| asyncio_websockets         | 772 ms                                                  | 751 ms: 1.03x faster                                                 |
| mdp                        | 3.80 sec                                                | 3.96 sec: 1.04x slower                                               |
| pathlib                    | 29.3 ms                                                 | 30.7 ms: 1.05x slower                                                |
| asyncio_tcp_ssl            | 2.79 sec                                                | 2.93 sec: 1.05x slower                                               |
| unpickle_list              | 6.67 us                                                 | 7.01 us: 1.05x slower                                                |
| async_generators           | 592 ms                                                  | 624 ms: 1.05x slower                                                 |
| python_startup             | 22.0 ms                                                 | 23.4 ms: 1.06x slower                                                |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 7.48 ms: 1.07x slower                                                |
| pidigits                   | 248 ms                                                  | 266 ms: 1.08x slower                                                 |
| python_startup_no_site     | 14.6 ms                                                 | 15.8 ms: 1.08x slower                                                |
| create_gc_cycles           | 2.46 ms                                                 | 2.65 ms: 1.08x slower                                                |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 983 ms: 1.09x slower                                                 |
| regex_effbot               | 4.84 ms                                                 | 5.30 ms: 1.09x slower                                                |
| async_tree_memoization     | 745 ms                                                  | 822 ms: 1.10x slower                                                 |
| regex_v8                   | 32.4 ms                                                 | 36.1 ms: 1.11x slower                                                |
| json_loads                 | 36.1 us                                                 | 40.2 us: 1.11x slower                                                |
| async_tree_io_tg           | 1.46 sec                                                | 1.62 sec: 1.12x slower                                               |
| tornado_http               | 248 ms                                                  | 279 ms: 1.12x slower                                                 |
| async_tree_none            | 576 ms                                                  | 656 ms: 1.14x slower                                                 |
| docutils                   | 4.01 sec                                                | 4.57 sec: 1.14x slower                                               |
| xml_etree_generate         | 129 ms                                                  | 148 ms: 1.14x slower                                                 |
| sympy_integrate            | 29.7 ms                                                 | 34.0 ms: 1.15x slower                                                |
| async_tree_io              | 1.38 sec                                                | 1.58 sec: 1.15x slower                                               |
| pylint                     | 472 ms                                                  | 542 ms: 1.15x slower                                                 |
| sympy_sum                  | 213 ms                                                  | 246 ms: 1.15x slower                                                 |
| sympy_str                  | 367 ms                                                  | 423 ms: 1.15x slower                                                 |
| sympy_expand               | 631 ms                                                  | 729 ms: 1.16x slower                                                 |
| nqueens                    | 108 ms                                                  | 125 ms: 1.16x slower                                                 |
| scimark_fft                | 477 ms                                                  | 555 ms: 1.17x slower                                                 |
| deepcopy_memo              | 51.7 us                                                 | 60.6 us: 1.17x slower                                                |
| deepcopy_reduce            | 4.27 us                                                 | 5.02 us: 1.18x slower                                                |
| bench_thread_pool          | 3.06 ms                                                 | 3.64 ms: 1.19x slower                                                |
| 2to3                       | 442 ms                                                  | 526 ms: 1.19x slower                                                 |
| async_tree_none_tg         | 521 ms                                                  | 620 ms: 1.19x slower                                                 |
| json_dumps                 | 14.9 ms                                                 | 17.8 ms: 1.20x slower                                                |
| thrift                     | 1.11 ms                                                 | 1.35 ms: 1.21x slower                                                |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 1.03 sec: 1.22x slower                                               |
| generators                 | 39.2 ms                                                 | 48.0 ms: 1.23x slower                                                |
| async_tree_memoization_tg  | 672 ms                                                  | 827 ms: 1.23x slower                                                 |
| fannkuch                   | 543 ms                                                  | 670 ms: 1.23x slower                                                 |
| bpe_tokeniser              | 6.25 sec                                                | 7.74 sec: 1.24x slower                                               |
| spectral_norm              | 159 ms                                                  | 198 ms: 1.24x slower                                                 |
| typing_runtime_protocols   | 216 us                                                  | 269 us: 1.25x slower                                                 |
| crypto_pyaes               | 99.8 ms                                                 | 126 ms: 1.27x slower                                                 |
| xml_etree_process          | 86.5 ms                                                 | 110 ms: 1.27x slower                                                 |
| richards                   | 65.8 ms                                                 | 84.3 ms: 1.28x slower                                                |
| tomli_loads                | 2.80 sec                                                | 3.60 sec: 1.29x slower                                               |
| html5lib                   | 98.1 ms                                                 | 128 ms: 1.30x slower                                                 |
| json                       | 6.55 ms                                                 | 8.58 ms: 1.31x slower                                                |
| sqlglot_optimize           | 76.2 ms                                                 | 99.9 ms: 1.31x slower                                                |
| pycparser                  | 1.57 sec                                                | 2.07 sec: 1.32x slower                                               |
| sqlglot_normalize          | 146 ms                                                  | 196 ms: 1.34x slower                                                 |
| pprint_pformat             | 2.00 sec                                                | 2.69 sec: 1.35x slower                                               |
| genshi_text                | 31.7 ms                                                 | 43.1 ms: 1.36x slower                                                |
| bench_mp_pool              | 19.4 ms                                                 | 26.3 ms: 1.36x slower                                                |
| genshi_xml                 | 68.3 ms                                                 | 94.1 ms: 1.38x slower                                                |
| coroutines                 | 29.2 ms                                                 | 40.5 ms: 1.39x slower                                                |
| django_template            | 46.9 ms                                                 | 65.8 ms: 1.40x slower                                                |
| pyflate                    | 661 ms                                                  | 934 ms: 1.41x slower                                                 |
| pprint_safe_repr           | 959 ms                                                  | 1.36 sec: 1.42x slower                                               |
| regex_compile              | 177 ms                                                  | 252 ms: 1.42x slower                                                 |
| float                      | 115 ms                                                  | 169 ms: 1.47x slower                                                 |
| unpickle_pure_python       | 296 us                                                  | 434 us: 1.47x slower                                                 |
| logging_simple             | 8.98 us                                                 | 13.3 us: 1.48x slower                                                |
| scimark_monte_carlo        | 89.9 ms                                                 | 134 ms: 1.49x slower                                                 |
| go                         | 195 ms                                                  | 291 ms: 1.49x slower                                                 |
| comprehensions             | 20.9 us                                                 | 31.3 us: 1.50x slower                                                |
| mako                       | 16.1 ms                                                 | 24.1 ms: 1.50x slower                                                |
| richards_super             | 76.3 ms                                                 | 117 ms: 1.53x slower                                                 |
| nbody                      | 124 ms                                                  | 191 ms: 1.55x slower                                                 |
| logging_format             | 9.48 us                                                 | 14.8 us: 1.56x slower                                                |
| chaos                      | 84.7 ms                                                 | 133 ms: 1.57x slower                                                 |
| sqlglot_transpile          | 2.30 ms                                                 | 3.62 ms: 1.57x slower                                                |
| sqlglot_parse              | 1.80 ms                                                 | 2.87 ms: 1.59x slower                                                |
| logging_silent             | 130 ns                                                  | 218 ns: 1.68x slower                                                 |
| scimark_lu                 | 154 ms                                                  | 259 ms: 1.68x slower                                                 |
| scimark_sor                | 172 ms                                                  | 290 ms: 1.69x slower                                                 |
| raytrace                   | 350 ms                                                  | 605 ms: 1.73x slower                                                 |
| hexiom                     | 8.35 ms                                                 | 15.0 ms: 1.80x slower                                                |
| pickle_pure_python         | 417 us                                                  | 755 us: 1.81x slower                                                 |
| deltablue                  | 4.56 ms                                                 | 9.49 ms: 2.08x slower                                                |
| Geometric mean             | (ref)                                                   | 1.23x slower                                                         |

Benchmark hidden because not significant (13): xml_etree_iterparse, xml_etree_parse, telco, meteor_contest, sqlite_synth, asyncio_tcp, coverage, pickle_list, deepcopy, regex_dna, gc_traversal, pickle_dict, pickle
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.00x