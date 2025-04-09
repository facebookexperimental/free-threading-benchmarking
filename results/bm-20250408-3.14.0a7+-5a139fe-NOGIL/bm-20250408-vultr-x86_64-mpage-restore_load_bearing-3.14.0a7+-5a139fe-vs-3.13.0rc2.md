# Results vs. 3.13.0rc2

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: 5a139fe
- commit date: 2025-04-08
- overall geometric mean: 1.040x slower
- HPT reliability: 99.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 70.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 538 ms: 1.67x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 567 ms: 1.56x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 293 ms: 1.40x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 486 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 516 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 193 ms: 1.12x faster                                                  |
| float          | 76.7 ms                                                                | 70.4 ms: 1.09x faster                                                 |
| nbody          | 85.3 ms                                                                | 116 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.2 ms: 1.09x faster                                                 |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.0 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                  |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 343 us: 1.18x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.48x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.5 ms: 1.19x slower                                                 |
| django_template | 34.2 ms                                                                | 41.9 ms: 1.23x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.3 ms: 1.26x slower                                                 |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.82 ms: 1.82x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.36 sec: 1.72x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 538 ms: 1.67x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 567 ms: 1.56x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 293 ms: 1.40x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 486 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 516 ms: 1.29x faster                                                  |
| deepcopy                   | 357 us                                                                 | 298 us: 1.20x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                                 |
| pidigits                   | 216 ms                                                                 | 193 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.2 ms: 1.09x faster                                                 |
| float                      | 76.7 ms                                                                | 70.4 ms: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.0 ms: 1.09x faster                                                 |
| go                         | 141 ms                                                                 | 133 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 128 ms: 1.04x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.7 us: 1.04x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 3.02 us: 1.03x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 73.7 ms: 1.01x faster                                                 |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 70.0 ms: 1.02x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 358 ms: 1.03x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.62 sec: 1.04x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.04x slower                                                |
| json                       | 4.98 ms                                                                | 5.24 ms: 1.05x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| pyflate                    | 449 ms                                                                 | 475 ms: 1.06x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.13 ms: 1.08x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.55 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 798 ms: 1.11x slower                                                  |
| 2to3                       | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                                  |
| chaos                      | 56.3 ms                                                                | 63.6 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.66 sec: 1.14x slower                                                |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| generators                 | 28.5 ms                                                                | 33.0 ms: 1.16x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 90.2 ms: 1.16x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.0 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 343 us: 1.18x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.5 ms: 1.18x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.07 ms: 1.19x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 134 ms: 1.19x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.32 us: 1.19x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.24 us: 1.19x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 58.5 ms: 1.19x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 545 ms: 1.20x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 329 ms: 1.20x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.1 us: 1.21x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.75 ms: 1.21x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.8 ms: 1.21x slower                                                 |
| raytrace                   | 250 ms                                                                 | 303 ms: 1.21x slower                                                  |
| richards_super             | 50.4 ms                                                                | 61.2 ms: 1.21x slower                                                 |
| django_template            | 34.2 ms                                                                | 41.9 ms: 1.23x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 463 ms: 1.23x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 84.6 ms: 1.24x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 27.3 ms: 1.26x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.26x slower                                                  |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.32x slower                                                  |
| nbody                      | 85.3 ms                                                                | 116 ms: 1.36x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 96.2 ms: 8.74x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a7+-5a139fe-NOGIL/bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.040x slower

# HPT report

- Reliability score: 99.42% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x