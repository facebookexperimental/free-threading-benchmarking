# Results vs. 3.13.0b1

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 719 ms: 1.63x slower                                                  |
| docutils       | 3.94 sec                                                              | 4.96 sec: 1.26x slower                                                |
| html5lib       | 92.0 ms                                                               | 139 ms: 1.51x slower                                                  |
| tornado_http   | 253 ms                                                                | 350 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.44x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.22x faster                                                |
| async_tree_memoization_tg | 692 ms                                                                | 660 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 952 ms: 1.06x slower                                                  |
| async_tree_none           | 523 ms                                                                | 610 ms: 1.17x slower                                                  |
| async_generators          | 588 ms                                                                | 734 ms: 1.25x slower                                                  |
| asyncio_tcp               | 972 ms                                                                | 1.22 sec: 1.25x slower                                                |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.56 sec: 1.26x slower                                                |
| coroutines                | 29.3 ms                                                               | 41.7 ms: 1.42x slower                                                 |
| Geometric mean            | (ref)                                                                 | 1.07x slower                                                          |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                | 204 ms: 1.78x slower                                                  |
| nbody          | 126 ms                                                                | 300 ms: 2.39x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.60x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 294 ms: 1.04x slower                                                  |
| regex_compile  | 189 ms                                                                | 284 ms: 1.50x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 40.9 us: 1.14x faster                                                 |
| pickle_list          | 7.48 us                                                               | 6.59 us: 1.14x faster                                                 |
| xml_etree_iterparse  | 163 ms                                                                | 171 ms: 1.05x slower                                                  |
| unpickle_list        | 6.78 us                                                               | 7.20 us: 1.06x slower                                                 |
| json_loads           | 37.9 us                                                               | 44.0 us: 1.16x slower                                                 |
| json_dumps           | 13.9 ms                                                               | 18.1 ms: 1.30x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 163 ms: 1.36x slower                                                  |
| tomli_loads          | 2.84 sec                                                              | 4.30 sec: 1.52x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 128 ms: 1.55x slower                                                  |
| unpickle_pure_python | 285 us                                                                | 550 us: 1.93x slower                                                  |
| pickle_pure_python   | 428 us                                                                | 870 us: 2.03x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                                          |

Benchmark hidden because not significant (3): unpickle, xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 21.5 ms: 1.35x slower                                                 |
| python_startup         | 23.5 ms                                                               | 32.8 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.6 ms                                                               | 55.1 ms: 1.74x slower                                                 |
| genshi_xml      | 71.9 ms                                                               | 129 ms: 1.80x slower                                                  |
| mako            | 16.7 ms                                                               | 30.1 ms: 1.81x slower                                                 |
| django_template | 46.1 ms                                                               | 85.9 ms: 1.86x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.80x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                     | 229 ms                                                                | 14.7 ms: 15.58x faster                                                |
| gc_traversal              | 5.80 ms                                                               | 4.60 ms: 1.26x faster                                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.22x faster                                                |
| create_gc_cycles          | 2.49 ms                                                               | 2.12 ms: 1.17x faster                                                 |
| pickle_dict               | 46.5 us                                                               | 40.9 us: 1.14x faster                                                 |
| pickle_list               | 7.48 us                                                               | 6.59 us: 1.14x faster                                                 |
| async_tree_memoization_tg | 692 ms                                                                | 660 ms: 1.05x faster                                                  |
| regex_dna                 | 284 ms                                                                | 294 ms: 1.04x slower                                                  |
| xml_etree_iterparse       | 163 ms                                                                | 171 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 952 ms: 1.06x slower                                                  |
| unpickle_list             | 6.78 us                                                               | 7.20 us: 1.06x slower                                                 |
| deepcopy                  | 498 us                                                                | 568 us: 1.14x slower                                                  |
| json_loads                | 37.9 us                                                               | 44.0 us: 1.16x slower                                                 |
| async_tree_none           | 523 ms                                                                | 610 ms: 1.17x slower                                                  |
| sqlite_synth              | 3.94 us                                                               | 4.60 us: 1.17x slower                                                 |
| pathlib                   | 31.8 ms                                                               | 37.2 ms: 1.17x slower                                                 |
| json                      | 6.79 ms                                                               | 8.10 ms: 1.19x slower                                                 |
| bench_mp_pool             | 19.7 ms                                                               | 24.0 ms: 1.22x slower                                                 |
| async_generators          | 588 ms                                                                | 734 ms: 1.25x slower                                                  |
| asyncio_tcp               | 972 ms                                                                | 1.22 sec: 1.25x slower                                                |
| docutils                  | 3.94 sec                                                              | 4.96 sec: 1.26x slower                                                |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.56 sec: 1.26x slower                                                |
| meteor_contest            | 156 ms                                                                | 199 ms: 1.27x slower                                                  |
| pycparser                 | 1.71 sec                                                              | 2.18 sec: 1.28x slower                                                |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 8.80 ms: 1.29x slower                                                 |
| mdp                       | 4.01 sec                                                              | 5.18 sec: 1.29x slower                                                |
| json_dumps                | 13.9 ms                                                               | 18.1 ms: 1.30x slower                                                 |
| coverage                  | 121 ms                                                                | 157 ms: 1.30x slower                                                  |
| deepcopy_memo             | 50.9 us                                                               | 67.4 us: 1.32x slower                                                 |
| generators                | 40.7 ms                                                               | 54.6 ms: 1.34x slower                                                 |
| pylint                    | 466 ms                                                                | 625 ms: 1.34x slower                                                  |
| python_startup_no_site    | 16.0 ms                                                               | 21.5 ms: 1.35x slower                                                 |
| xml_etree_generate        | 120 ms                                                                | 163 ms: 1.36x slower                                                  |
| tornado_http              | 253 ms                                                                | 350 ms: 1.38x slower                                                  |
| deepcopy_reduce           | 4.31 us                                                               | 5.97 us: 1.39x slower                                                 |
| scimark_fft               | 469 ms                                                                | 652 ms: 1.39x slower                                                  |
| python_startup            | 23.5 ms                                                               | 32.8 ms: 1.40x slower                                                 |
| coroutines                | 29.3 ms                                                               | 41.7 ms: 1.42x slower                                                 |
| regex_compile             | 189 ms                                                                | 284 ms: 1.50x slower                                                  |
| html5lib                  | 92.0 ms                                                               | 139 ms: 1.51x slower                                                  |
| tomli_loads               | 2.84 sec                                                              | 4.30 sec: 1.52x slower                                                |
| pyflate                   | 710 ms                                                                | 1.08 sec: 1.52x slower                                                |
| crypto_pyaes              | 102 ms                                                                | 156 ms: 1.53x slower                                                  |
| fannkuch                  | 535 ms                                                                | 831 ms: 1.55x slower                                                  |
| xml_etree_process         | 82.2 ms                                                               | 128 ms: 1.55x slower                                                  |
| dulwich_log               | 97.5 ms                                                               | 152 ms: 1.56x slower                                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 10.2 sec: 1.57x slower                                                |
| thrift                    | 1.09 ms                                                               | 1.70 ms: 1.57x slower                                                 |
| typing_runtime_protocols  | 222 us                                                                | 353 us: 1.59x slower                                                  |
| sqlglot_normalize         | 150 ms                                                                | 240 ms: 1.60x slower                                                  |
| nqueens                   | 108 ms                                                                | 174 ms: 1.61x slower                                                  |
| 2to3                      | 441 ms                                                                | 719 ms: 1.63x slower                                                  |
| spectral_norm             | 151 ms                                                                | 249 ms: 1.65x slower                                                  |
| comprehensions            | 22.6 us                                                               | 37.3 us: 1.65x slower                                                 |
| logging_format            | 9.36 us                                                               | 15.5 us: 1.65x slower                                                 |
| richards                  | 68.8 ms                                                               | 114 ms: 1.66x slower                                                  |
| sqlglot_optimize          | 77.9 ms                                                               | 130 ms: 1.67x slower                                                  |
| richards_super            | 73.5 ms                                                               | 123 ms: 1.68x slower                                                  |
| sympy_integrate           | 28.7 ms                                                               | 48.3 ms: 1.68x slower                                                 |
| pprint_safe_repr          | 991 ms                                                                | 1.68 sec: 1.69x slower                                                |
| pprint_pformat            | 2.04 sec                                                              | 3.48 sec: 1.71x slower                                                |
| genshi_text               | 31.6 ms                                                               | 55.1 ms: 1.74x slower                                                 |
| float                     | 115 ms                                                                | 204 ms: 1.78x slower                                                  |
| scimark_monte_carlo       | 89.0 ms                                                               | 160 ms: 1.80x slower                                                  |
| genshi_xml                | 71.9 ms                                                               | 129 ms: 1.80x slower                                                  |
| mako                      | 16.7 ms                                                               | 30.1 ms: 1.81x slower                                                 |
| bench_thread_pool         | 3.01 ms                                                               | 5.45 ms: 1.81x slower                                                 |
| sympy_str                 | 376 ms                                                                | 696 ms: 1.85x slower                                                  |
| django_template           | 46.1 ms                                                               | 85.9 ms: 1.86x slower                                                 |
| go                        | 193 ms                                                                | 361 ms: 1.87x slower                                                  |
| logging_silent            | 137 ns                                                                | 260 ns: 1.90x slower                                                  |
| unpickle_pure_python      | 285 us                                                                | 550 us: 1.93x slower                                                  |
| scimark_sor               | 176 ms                                                                | 340 ms: 1.93x slower                                                  |
| logging_simple            | 9.16 us                                                               | 17.7 us: 1.94x slower                                                 |
| sqlglot_parse             | 1.92 ms                                                               | 3.72 ms: 1.94x slower                                                 |
| hexiom                    | 8.42 ms                                                               | 16.4 ms: 1.95x slower                                                 |
| sqlglot_transpile         | 2.24 ms                                                               | 4.43 ms: 1.98x slower                                                 |
| pickle_pure_python        | 428 us                                                                | 870 us: 2.03x slower                                                  |
| scimark_lu                | 150 ms                                                                | 305 ms: 2.03x slower                                                  |
| sympy_expand              | 638 ms                                                                | 1.33 sec: 2.09x slower                                                |
| raytrace                  | 351 ms                                                                | 751 ms: 2.14x slower                                                  |
| chaos                     | 81.5 ms                                                               | 176 ms: 2.16x slower                                                  |
| sympy_sum                 | 226 ms                                                                | 492 ms: 2.17x slower                                                  |
| nbody                     | 126 ms                                                                | 300 ms: 2.39x slower                                                  |
| deltablue                 | 4.55 ms                                                               | 11.3 ms: 2.50x slower                                                 |
| unpack_sequence           | 54.6 ns                                                               | 180 ns: 3.29x slower                                                  |
| Geometric mean            | (ref)                                                                 | 1.38x slower                                                          |

Benchmark hidden because not significant (11): async_tree_memoization, async_tree_io, pidigits, async_tree_none_tg, unpickle, async_tree_cpu_io_mixed_tg, xml_etree_parse, pickle, regex_v8, asyncio_websockets, regex_effbot
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x