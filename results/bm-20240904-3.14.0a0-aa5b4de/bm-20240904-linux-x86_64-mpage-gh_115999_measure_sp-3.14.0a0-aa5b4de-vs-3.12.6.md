# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_measure_sp
- machine: linux-x86_64
- commit hash: aa5b4de
- commit date: 2024-09-04
- overall geometric mean: 1.20x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 526 ms: 1.15x slower                                                 |
| docutils       | 4.00 sec                                               | 4.57 sec: 1.14x slower                                               |
| html5lib       | 88.9 ms                                                | 128 ms: 1.44x slower                                                 |
| Geometric mean | (ref)                                                  | 1.19x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.62 sec: 1.19x faster                                               |
| async_tree_memoization     | 977 ms                                                 | 822 ms: 1.19x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.58 sec: 1.17x faster                                               |
| async_tree_none_tg         | 704 ms                                                 | 620 ms: 1.13x faster                                                 |
| async_tree_none            | 741 ms                                                 | 656 ms: 1.13x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 827 ms: 1.12x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 983 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 1.03 sec: 1.06x faster                                               |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.93 sec: 1.04x slower                                               |
| async_generators           | 589 ms                                                 | 624 ms: 1.06x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 997 ms: 1.08x slower                                                 |
| coroutines                 | 29.5 ms                                                | 40.5 ms: 1.37x slower                                                |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 266 ms: 1.07x slower                                                 |
| float          | 123 ms                                                 | 169 ms: 1.37x slower                                                 |
| nbody          | 119 ms                                                 | 191 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                  | 1.33x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 296 ms: 1.07x slower                                                 |
| regex_v8       | 32.5 ms                                                | 36.1 ms: 1.11x slower                                                |
| regex_compile  | 187 ms                                                 | 252 ms: 1.35x slower                                                 |
| Geometric mean | (ref)                                                  | 1.13x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 21.2 us                                                | 19.3 us: 1.10x faster                                                |
| pickle_dict          | 52.7 us                                                | 48.3 us: 1.09x faster                                                |
| json_loads           | 37.9 us                                                | 40.2 us: 1.06x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 148 ms: 1.16x slower                                                 |
| json_dumps           | 14.3 ms                                                | 17.8 ms: 1.25x slower                                                |
| tomli_loads          | 2.88 sec                                               | 3.60 sec: 1.25x slower                                               |
| xml_etree_process    | 83.7 ms                                                | 110 ms: 1.31x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 434 us: 1.45x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 755 us: 1.73x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                         |

Benchmark hidden because not significant (5): xml_etree_iterparse, xml_etree_parse, pickle, pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.8 ms: 1.12x faster                                                |
| Geometric mean         | (ref)                                                  | 1.06x faster                                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 94.1 ms: 1.39x slower                                                |
| genshi_text     | 30.2 ms                                                | 43.1 ms: 1.43x slower                                                |
| django_template | 44.9 ms                                                | 65.8 ms: 1.46x slower                                                |
| mako            | 15.7 ms                                                | 24.1 ms: 1.53x slower                                                |
| Geometric mean  | (ref)                                                  | 1.45x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.62 sec: 1.19x faster                                               |
| async_tree_memoization     | 977 ms                                                 | 822 ms: 1.19x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.58 sec: 1.17x faster                                               |
| async_tree_none_tg         | 704 ms                                                 | 620 ms: 1.13x faster                                                 |
| async_tree_none            | 741 ms                                                 | 656 ms: 1.13x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 827 ms: 1.12x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 15.8 ms: 1.12x faster                                                |
| unpickle                   | 21.2 us                                                | 19.3 us: 1.10x faster                                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 983 ms: 1.10x faster                                                 |
| pickle_dict                | 52.7 us                                                | 48.3 us: 1.09x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 1.03 sec: 1.06x faster                                               |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.93 sec: 1.04x slower                                               |
| async_generators           | 589 ms                                                 | 624 ms: 1.06x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.11 us: 1.06x slower                                                |
| json_loads                 | 37.9 us                                                | 40.2 us: 1.06x slower                                                |
| regex_dna                  | 278 ms                                                 | 296 ms: 1.07x slower                                                 |
| pidigits                   | 250 ms                                                 | 266 ms: 1.07x slower                                                 |
| nqueens                    | 117 ms                                                 | 125 ms: 1.07x slower                                                 |
| meteor_contest             | 146 ms                                                 | 158 ms: 1.08x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 997 ms: 1.08x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 65.7 ns: 1.09x slower                                                |
| sympy_str                  | 385 ms                                                 | 423 ms: 1.10x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 246 ms: 1.11x slower                                                 |
| regex_v8                   | 32.5 ms                                                | 36.1 ms: 1.11x slower                                                |
| scimark_fft                | 500 ms                                                 | 555 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.48 ms: 1.12x slower                                                |
| sympy_integrate            | 29.8 ms                                                | 34.0 ms: 1.14x slower                                                |
| docutils                   | 4.00 sec                                               | 4.57 sec: 1.14x slower                                               |
| 2to3                       | 456 ms                                                 | 526 ms: 1.15x slower                                                 |
| deepcopy_memo              | 52.4 us                                                | 60.6 us: 1.16x slower                                                |
| comprehensions             | 27.1 us                                                | 31.3 us: 1.16x slower                                                |
| pycparser                  | 1.79 sec                                               | 2.07 sec: 1.16x slower                                               |
| xml_etree_generate         | 127 ms                                                 | 148 ms: 1.16x slower                                                 |
| pylint                     | 465 ms                                                 | 542 ms: 1.17x slower                                                 |
| generators                 | 41.1 ms                                                | 48.0 ms: 1.17x slower                                                |
| bpe_tokeniser              | 6.59 sec                                               | 7.74 sec: 1.17x slower                                               |
| crypto_pyaes               | 107 ms                                                 | 126 ms: 1.18x slower                                                 |
| coverage                   | 95.4 ms                                                | 112 ms: 1.18x slower                                                 |
| telco                      | 9.59 ms                                                | 11.4 ms: 1.18x slower                                                |
| typing_runtime_protocols   | 224 us                                                 | 269 us: 1.20x slower                                                 |
| fannkuch                   | 540 ms                                                 | 670 ms: 1.24x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 5.02 us: 1.24x slower                                                |
| json_dumps                 | 14.3 ms                                                | 17.8 ms: 1.25x slower                                                |
| sqlglot_normalize          | 157 ms                                                 | 196 ms: 1.25x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 3.60 sec: 1.25x slower                                               |
| json                       | 6.85 ms                                                | 8.58 ms: 1.25x slower                                                |
| sympy_expand               | 582 ms                                                 | 729 ms: 1.25x slower                                                 |
| spectral_norm              | 156 ms                                                 | 198 ms: 1.27x slower                                                 |
| bench_mp_pool              | 20.7 ms                                                | 26.3 ms: 1.27x slower                                                |
| thrift                     | 1.06 ms                                                | 1.35 ms: 1.28x slower                                                |
| pyflate                    | 727 ms                                                 | 934 ms: 1.28x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 110 ms: 1.31x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 99.9 ms: 1.32x slower                                                |
| regex_compile              | 187 ms                                                 | 252 ms: 1.35x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.69 sec: 1.36x slower                                               |
| create_gc_cycles           | 1.94 ms                                                | 2.65 ms: 1.37x slower                                                |
| float                      | 123 ms                                                 | 169 ms: 1.37x slower                                                 |
| coroutines                 | 29.5 ms                                                | 40.5 ms: 1.37x slower                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 134 ms: 1.39x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 94.1 ms: 1.39x slower                                                |
| richards                   | 60.3 ms                                                | 84.3 ms: 1.40x slower                                                |
| pprint_safe_repr           | 967 ms                                                 | 1.36 sec: 1.40x slower                                               |
| logging_simple             | 9.45 us                                                | 13.3 us: 1.41x slower                                                |
| genshi_text                | 30.2 ms                                                | 43.1 ms: 1.43x slower                                                |
| html5lib                   | 88.9 ms                                                | 128 ms: 1.44x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 434 us: 1.45x slower                                                 |
| django_template            | 44.9 ms                                                | 65.8 ms: 1.46x slower                                                |
| raytrace                   | 408 ms                                                 | 605 ms: 1.48x slower                                                 |
| mako                       | 15.7 ms                                                | 24.1 ms: 1.53x slower                                                |
| logging_format             | 9.59 us                                                | 14.8 us: 1.54x slower                                                |
| sqlglot_transpile          | 2.34 ms                                                | 3.62 ms: 1.55x slower                                                |
| logging_silent             | 139 ns                                                 | 218 ns: 1.57x slower                                                 |
| chaos                      | 84.9 ms                                                | 133 ms: 1.57x slower                                                 |
| sqlglot_parse              | 1.79 ms                                                | 2.87 ms: 1.60x slower                                                |
| nbody                      | 119 ms                                                 | 191 ms: 1.61x slower                                                 |
| richards_super             | 72.8 ms                                                | 117 ms: 1.61x slower                                                 |
| go                         | 172 ms                                                 | 291 ms: 1.69x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 259 ms: 1.70x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 755 us: 1.73x slower                                                 |
| scimark_sor                | 167 ms                                                 | 290 ms: 1.74x slower                                                 |
| hexiom                     | 8.27 ms                                                | 15.0 ms: 1.81x slower                                                |
| deltablue                  | 4.27 ms                                                | 9.49 ms: 2.22x slower                                                |
| Geometric mean             | (ref)                                                  | 1.20x slower                                                         |

Benchmark hidden because not significant (14): xml_etree_iterparse, pathlib, xml_etree_parse, pickle, python_startup, mdp, pickle_list, asyncio_websockets, unpickle_list, regex_effbot, gc_traversal, bench_thread_pool, tornado_http, deepcopy
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.01x