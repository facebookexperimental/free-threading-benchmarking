# Results vs. 3.13.0rc2

- fork: python
- ref: cc0e59f17d0fcd8ed9f3
- machine: linux-x86_64
- commit hash: cc0e59f
- commit date: 2026-11-25
- overall geometric mean: 1.056x slower
- HPT reliability: 85.84%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 289 ms: 1.12x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                    |
| html5lib       | 68.6 ms                                                                | 66.9 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 699 ms: 1.29x faster                                                      |
| async_generators           | 375 ms                                                                 | 293 ms: 1.28x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 728 ms: 1.21x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 586 ms: 1.14x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 411 ms: 1.12x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 576 ms: 1.10x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 395 ms: 1.04x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 502 ms: 1.03x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 26.2 ms: 1.12x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.10x faster                                                              |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 177 ms: 1.22x faster                                                      |
| float          | 76.7 ms                                                                | 83.4 ms: 1.09x slower                                                     |
| nbody          | 85.3 ms                                                                | 116 ms: 1.36x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 20.8 ms: 1.12x faster                                                     |
| regex_dna      | 189 ms                                                                 | 171 ms: 1.10x faster                                                      |
| regex_compile  | 131 ms                                                                 | 168 ms: 1.28x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.91 ms: 1.07x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.93 sec: 1.04x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                                     |
| json_loads           | 27.3 us                                                                | 30.7 us: 1.12x slower                                                     |
| unpickle_pure_python | 208 us                                                                 | 238 us: 1.14x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 343 us: 1.18x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 72.8 ms: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.93 ms: 1.20x slower                                                     |
| python_startup         | 11.0 ms                                                                | 13.5 ms: 1.22x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.21x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.4 ms: 1.18x slower                                                     |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.76x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 1.83 ms: 1.82x faster                                                     |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.80x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 6.60 ms: 1.67x faster                                                     |
| deepcopy                   | 357 us                                                                 | 268 us: 1.33x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 699 ms: 1.29x faster                                                      |
| async_generators           | 375 ms                                                                 | 293 ms: 1.28x faster                                                      |
| pidigits                   | 216 ms                                                                 | 177 ms: 1.22x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 728 ms: 1.21x faster                                                      |
| go                         | 141 ms                                                                 | 119 ms: 1.18x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 33.4 us: 1.14x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 586 ms: 1.14x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 137 us: 1.13x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 1.99 us: 1.13x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 119 ms: 1.12x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 411 ms: 1.12x faster                                                      |
| regex_v8                   | 23.2 ms                                                                | 20.8 ms: 1.12x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 171 ms: 1.10x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 576 ms: 1.10x faster                                                      |
| json_dumps                 | 10.6 ms                                                                | 9.91 ms: 1.07x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 18.1 ms: 1.06x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.94 us: 1.06x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.06x faster                                                      |
| scimark_fft                | 348 ms                                                                 | 330 ms: 1.06x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.26 sec: 1.05x faster                                                    |
| tomli_loads                | 2.01 sec                                                               | 1.93 sec: 1.04x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 395 ms: 1.04x faster                                                      |
| dulwich_log                | 74.5 ms                                                                | 71.9 ms: 1.04x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 502 ms: 1.03x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 66.9 ms: 1.03x faster                                                     |
| pyflate                    | 449 ms                                                                 | 444 ms: 1.01x faster                                                      |
| xml_etree_iterparse        | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.00 ms: 1.05x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                    |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 120 ms: 1.07x slower                                                      |
| logging_silent             | 98.2 ns                                                                | 106 ns: 1.08x slower                                                      |
| chaos                      | 56.3 ms                                                                | 60.8 ms: 1.08x slower                                                     |
| float                      | 76.7 ms                                                                | 83.4 ms: 1.09x slower                                                     |
| json                       | 4.98 ms                                                                | 5.43 ms: 1.09x slower                                                     |
| comprehensions             | 16.6 us                                                                | 18.1 us: 1.09x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 6.53 ms: 1.10x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.11x slower                                                     |
| 2to3                       | 259 ms                                                                 | 289 ms: 1.12x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                                     |
| json_loads                 | 27.3 us                                                                | 30.7 us: 1.12x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 26.2 ms: 1.12x slower                                                     |
| nqueens                    | 77.7 ms                                                                | 87.4 ms: 1.12x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 814 ms: 1.13x slower                                                      |
| generators                 | 28.5 ms                                                                | 32.6 ms: 1.14x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 238 us: 1.14x slower                                                      |
| logging_simple             | 6.14 us                                                                | 7.06 us: 1.15x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.16x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 318 ms: 1.16x slower                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.8 ms: 1.17x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 531 ms: 1.17x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.63 ms: 1.17x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.17x slower                                                      |
| logging_format             | 6.92 us                                                                | 8.13 us: 1.18x slower                                                     |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 343 us: 1.18x slower                                                      |
| django_template            | 34.2 ms                                                                | 40.4 ms: 1.18x slower                                                     |
| richards                   | 44.4 ms                                                                | 52.4 ms: 1.18x slower                                                     |
| richards_super             | 50.4 ms                                                                | 59.7 ms: 1.19x slower                                                     |
| thrift                     | 772 us                                                                 | 927 us: 1.20x slower                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 8.93 ms: 1.20x slower                                                     |
| python_startup             | 11.0 ms                                                                | 13.5 ms: 1.22x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 72.8 ms: 1.23x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 125 ms: 1.23x slower                                                      |
| fannkuch                   | 376 ms                                                                 | 464 ms: 1.24x slower                                                      |
| regex_compile              | 131 ms                                                                 | 168 ms: 1.28x slower                                                      |
| crypto_pyaes               | 68.2 ms                                                                | 88.2 ms: 1.29x slower                                                     |
| nbody                      | 85.3 ms                                                                | 116 ms: 1.36x slower                                                      |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                     |
| coverage                   | 82.5 ms                                                                | 118 ms: 1.44x slower                                                      |
| bench_thread_pool          | 924 us                                                                 | 1.40 ms: 1.52x slower                                                     |
| telco                      | 7.77 ms                                                                | 173 ms: 22.21x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                              |

Benchmark hidden because not significant (1): async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261125-3.16.0a2+dev-cc0e59f-NOGIL/bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.056x slower

# HPT report

- Reliability score: 85.84% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x