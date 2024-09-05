# Results vs. 3.13.0b1

- fork: mpage
- ref: f4d1deda87c7c7bcf4b1
- machine: linux-x86_64
- commit hash: f4d1ded
- commit date: 2024-09-04
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 546 ms: 1.24x slower                                                 |
| docutils       | 3.94 sec                                                              | 4.52 sec: 1.15x slower                                               |
| html5lib       | 92.0 ms                                                               | 130 ms: 1.41x slower                                                 |
| tornado_http   | 253 ms                                                                | 334 ms: 1.32x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.27x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.83 sec                                                              | 2.75 sec: 1.03x faster                                               |
| asyncio_websockets         | 728 ms                                                                | 752 ms: 1.03x slower                                                 |
| async_generators           | 588 ms                                                                | 637 ms: 1.08x slower                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.56 sec: 1.09x slower                                               |
| async_tree_memoization_tg  | 692 ms                                                                | 760 ms: 1.10x slower                                                 |
| async_tree_io              | 1.39 sec                                                              | 1.55 sec: 1.12x slower                                               |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 1.01 sec: 1.12x slower                                               |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 1.01 sec: 1.15x slower                                               |
| async_tree_none_tg         | 526 ms                                                                | 609 ms: 1.16x slower                                                 |
| async_tree_none            | 523 ms                                                                | 636 ms: 1.22x slower                                                 |
| coroutines                 | 29.3 ms                                                               | 38.7 ms: 1.32x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.10x slower                                                         |

Benchmark hidden because not significant (2): asyncio_tcp, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 115 ms                                                                | 171 ms: 1.49x slower                                                 |
| nbody          | 126 ms                                                                | 226 ms: 1.80x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.38x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 304 ms: 1.07x slower                                                 |
| regex_compile  | 189 ms                                                                | 253 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                         |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 22.2 us                                                               | 19.4 us: 1.15x faster                                                |
| pickle_list          | 7.48 us                                                               | 6.68 us: 1.12x faster                                                |
| json_loads           | 37.9 us                                                               | 40.3 us: 1.07x slower                                                |
| unpickle_list        | 6.78 us                                                               | 7.52 us: 1.11x slower                                                |
| xml_etree_generate   | 120 ms                                                                | 142 ms: 1.18x slower                                                 |
| json_dumps           | 13.9 ms                                                               | 16.8 ms: 1.20x slower                                                |
| xml_etree_iterparse  | 163 ms                                                                | 196 ms: 1.21x slower                                                 |
| tomli_loads          | 2.84 sec                                                              | 3.74 sec: 1.32x slower                                               |
| xml_etree_process    | 82.2 ms                                                               | 110 ms: 1.33x slower                                                 |
| pickle_pure_python   | 428 us                                                                | 673 us: 1.57x slower                                                 |
| unpickle_pure_python | 285 us                                                                | 461 us: 1.62x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.15x slower                                                         |

Benchmark hidden because not significant (3): pickle_dict, pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.7 ms                                                               | 22.5 ms: 1.35x slower                                                |
| genshi_text     | 31.6 ms                                                               | 43.7 ms: 1.38x slower                                                |
| django_template | 46.1 ms                                                               | 64.3 ms: 1.39x slower                                                |
| genshi_xml      | 71.9 ms                                                               | 101 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.38x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 12.0 ms: 19.04x faster                                               |
| unpickle                   | 22.2 us                                                               | 19.4 us: 1.15x faster                                                |
| pickle_list                | 7.48 us                                                               | 6.68 us: 1.12x faster                                                |
| coverage                   | 121 ms                                                                | 114 ms: 1.06x faster                                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 2.75 sec: 1.03x faster                                               |
| asyncio_websockets         | 728 ms                                                                | 752 ms: 1.03x slower                                                 |
| deepcopy_reduce            | 4.31 us                                                               | 4.47 us: 1.04x slower                                                |
| deepcopy_memo              | 50.9 us                                                               | 53.1 us: 1.04x slower                                                |
| pathlib                    | 31.8 ms                                                               | 33.7 ms: 1.06x slower                                                |
| json_loads                 | 37.9 us                                                               | 40.3 us: 1.07x slower                                                |
| regex_dna                  | 284 ms                                                                | 304 ms: 1.07x slower                                                 |
| meteor_contest             | 156 ms                                                                | 168 ms: 1.07x slower                                                 |
| async_generators           | 588 ms                                                                | 637 ms: 1.08x slower                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.56 sec: 1.09x slower                                               |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 7.49 ms: 1.10x slower                                                |
| async_tree_memoization_tg  | 692 ms                                                                | 760 ms: 1.10x slower                                                 |
| unpickle_list              | 6.78 us                                                               | 7.52 us: 1.11x slower                                                |
| gc_traversal               | 5.80 ms                                                               | 6.46 ms: 1.11x slower                                                |
| async_tree_io              | 1.39 sec                                                              | 1.55 sec: 1.12x slower                                               |
| sqlite_synth               | 3.94 us                                                               | 4.40 us: 1.12x slower                                                |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 1.01 sec: 1.12x slower                                               |
| json                       | 6.79 ms                                                               | 7.67 ms: 1.13x slower                                                |
| scimark_fft                | 469 ms                                                                | 538 ms: 1.15x slower                                                 |
| docutils                   | 3.94 sec                                                              | 4.52 sec: 1.15x slower                                               |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 1.01 sec: 1.15x slower                                               |
| sympy_sum                  | 226 ms                                                                | 260 ms: 1.15x slower                                                 |
| async_tree_none_tg         | 526 ms                                                                | 609 ms: 1.16x slower                                                 |
| bpe_tokeniser              | 6.53 sec                                                              | 7.57 sec: 1.16x slower                                               |
| sympy_expand               | 638 ms                                                                | 742 ms: 1.16x slower                                                 |
| bench_mp_pool              | 19.7 ms                                                               | 23.1 ms: 1.17x slower                                                |
| xml_etree_generate         | 120 ms                                                                | 142 ms: 1.18x slower                                                 |
| generators                 | 40.7 ms                                                               | 48.5 ms: 1.19x slower                                                |
| json_dumps                 | 13.9 ms                                                               | 16.8 ms: 1.20x slower                                                |
| pycparser                  | 1.71 sec                                                              | 2.06 sec: 1.20x slower                                               |
| xml_etree_iterparse        | 163 ms                                                                | 196 ms: 1.21x slower                                                 |
| pylint                     | 466 ms                                                                | 563 ms: 1.21x slower                                                 |
| async_tree_none            | 523 ms                                                                | 636 ms: 1.22x slower                                                 |
| sympy_integrate            | 28.7 ms                                                               | 35.0 ms: 1.22x slower                                                |
| 2to3                       | 441 ms                                                                | 546 ms: 1.24x slower                                                 |
| typing_runtime_protocols   | 222 us                                                                | 275 us: 1.24x slower                                                 |
| nqueens                    | 108 ms                                                                | 136 ms: 1.25x slower                                                 |
| sympy_str                  | 376 ms                                                                | 480 ms: 1.28x slower                                                 |
| fannkuch                   | 535 ms                                                                | 688 ms: 1.29x slower                                                 |
| richards                   | 68.8 ms                                                               | 90.4 ms: 1.31x slower                                                |
| tomli_loads                | 2.84 sec                                                              | 3.74 sec: 1.32x slower                                               |
| coroutines                 | 29.3 ms                                                               | 38.7 ms: 1.32x slower                                                |
| tornado_http               | 253 ms                                                                | 334 ms: 1.32x slower                                                 |
| regex_compile              | 189 ms                                                                | 253 ms: 1.33x slower                                                 |
| thrift                     | 1.09 ms                                                               | 1.45 ms: 1.33x slower                                                |
| xml_etree_process          | 82.2 ms                                                               | 110 ms: 1.33x slower                                                 |
| crypto_pyaes               | 102 ms                                                                | 137 ms: 1.35x slower                                                 |
| mako                       | 16.7 ms                                                               | 22.5 ms: 1.35x slower                                                |
| pyflate                    | 710 ms                                                                | 961 ms: 1.35x slower                                                 |
| pprint_pformat             | 2.04 sec                                                              | 2.76 sec: 1.36x slower                                               |
| sqlglot_normalize          | 150 ms                                                                | 205 ms: 1.36x slower                                                 |
| sqlglot_optimize           | 77.9 ms                                                               | 106 ms: 1.36x slower                                                 |
| comprehensions             | 22.6 us                                                               | 31.0 us: 1.37x slower                                                |
| genshi_text                | 31.6 ms                                                               | 43.7 ms: 1.38x slower                                                |
| bench_thread_pool          | 3.01 ms                                                               | 4.17 ms: 1.39x slower                                                |
| django_template            | 46.1 ms                                                               | 64.3 ms: 1.39x slower                                                |
| pprint_safe_repr           | 991 ms                                                                | 1.39 sec: 1.41x slower                                               |
| logging_simple             | 9.16 us                                                               | 12.9 us: 1.41x slower                                                |
| genshi_xml                 | 71.9 ms                                                               | 101 ms: 1.41x slower                                                 |
| html5lib                   | 92.0 ms                                                               | 130 ms: 1.41x slower                                                 |
| spectral_norm              | 151 ms                                                                | 216 ms: 1.43x slower                                                 |
| float                      | 115 ms                                                                | 171 ms: 1.49x slower                                                 |
| richards_super             | 73.5 ms                                                               | 111 ms: 1.51x slower                                                 |
| sqlglot_parse              | 1.92 ms                                                               | 2.93 ms: 1.53x slower                                                |
| go                         | 193 ms                                                                | 298 ms: 1.54x slower                                                 |
| logging_silent             | 137 ns                                                                | 214 ns: 1.56x slower                                                 |
| pickle_pure_python         | 428 us                                                                | 673 us: 1.57x slower                                                 |
| chaos                      | 81.5 ms                                                               | 129 ms: 1.58x slower                                                 |
| unpickle_pure_python       | 285 us                                                                | 461 us: 1.62x slower                                                 |
| sqlglot_transpile          | 2.24 ms                                                               | 3.66 ms: 1.63x slower                                                |
| logging_format             | 9.36 us                                                               | 15.4 us: 1.64x slower                                                |
| hexiom                     | 8.42 ms                                                               | 13.9 ms: 1.65x slower                                                |
| scimark_monte_carlo        | 89.0 ms                                                               | 147 ms: 1.65x slower                                                 |
| scimark_sor                | 176 ms                                                                | 304 ms: 1.72x slower                                                 |
| raytrace                   | 351 ms                                                                | 608 ms: 1.73x slower                                                 |
| scimark_lu                 | 150 ms                                                                | 261 ms: 1.74x slower                                                 |
| nbody                      | 126 ms                                                                | 226 ms: 1.80x slower                                                 |
| deltablue                  | 4.55 ms                                                               | 9.01 ms: 1.98x slower                                                |
| unpack_sequence            | 54.6 ns                                                               | 149 ns: 2.72x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.21x slower                                                         |

Benchmark hidden because not significant (13): create_gc_cycles, pickle_dict, pidigits, deepcopy, pickle, asyncio_tcp, python_startup, mdp, python_startup_no_site, xml_etree_parse, regex_v8, async_tree_memoization, regex_effbot
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.00x