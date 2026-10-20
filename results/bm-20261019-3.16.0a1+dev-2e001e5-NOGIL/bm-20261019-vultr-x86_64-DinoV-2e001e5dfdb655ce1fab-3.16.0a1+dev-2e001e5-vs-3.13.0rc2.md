# Results vs. 3.13.0rc2

- fork: DinoV
- ref: 2e001e5dfdb655ce1fab
- machine: linux-x86_64
- commit hash: 2e001e5
- commit date: 2026-10-19
- overall geometric mean: 1.078x slower
- HPT reliability: 93.47%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 304 ms: 1.17x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.98 sec: 1.13x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 705 ms: 1.28x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 723 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 596 ms: 1.12x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 416 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 580 ms: 1.09x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 337 ms: 1.05x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 395 ms: 1.04x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 499 ms: 1.04x faster                                                     |
| async_generators           | 375 ms                                                                 | 421 ms: 1.12x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 26.2 ms: 1.13x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                             |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 183 ms: 1.18x faster                                                     |
| float          | 76.7 ms                                                                | 86.3 ms: 1.12x slower                                                    |
| nbody          | 85.3 ms                                                                | 122 ms: 1.43x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 21.2 ms: 1.09x faster                                                    |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.06x faster                                                     |
| regex_compile  | 131 ms                                                                 | 172 ms: 1.31x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                   |
| json_dumps           | 10.6 ms                                                                | 10.4 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 97.2 ms: 1.03x slower                                                    |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                     |
| json_loads           | 27.3 us                                                                | 30.3 us: 1.11x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 337 us: 1.15x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 104 ms: 1.21x slower                                                     |
| xml_etree_process    | 59.2 ms                                                                | 77.6 ms: 1.31x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                                    |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.38x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                    |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.33x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 135 ms: 2.35x faster                                                     |
| gc_traversal               | 3.32 ms                                                                | 1.82 ms: 1.82x faster                                                    |
| mdp                        | 2.34 sec                                                               | 1.41 sec: 1.66x faster                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 7.34 ms: 1.50x faster                                                    |
| deepcopy                   | 357 us                                                                 | 273 us: 1.31x faster                                                     |
| async_tree_io_tg           | 901 ms                                                                 | 705 ms: 1.28x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 723 ms: 1.22x faster                                                     |
| pidigits                   | 216 ms                                                                 | 183 ms: 1.18x faster                                                     |
| go                         | 141 ms                                                                 | 119 ms: 1.18x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 1.92 us: 1.17x faster                                                    |
| deepcopy_memo              | 38.1 us                                                                | 33.2 us: 1.15x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 596 ms: 1.12x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.12x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 416 ms: 1.11x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.2 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 580 ms: 1.09x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 320 ms: 1.09x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.06x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 101 ms: 1.06x faster                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 147 us: 1.06x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 337 ms: 1.05x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 18.4 ms: 1.04x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 395 ms: 1.04x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 499 ms: 1.04x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 71.9 ms: 1.04x faster                                                    |
| pyflate                    | 449 ms                                                                 | 436 ms: 1.03x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 3.03 us: 1.03x faster                                                    |
| json_dumps                 | 10.6 ms                                                                | 10.4 ms: 1.03x faster                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.38 sec: 1.02x faster                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.33 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 97.2 ms: 1.03x slower                                                    |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                     |
| chaos                      | 56.3 ms                                                                | 59.9 ms: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                   |
| json                       | 4.98 ms                                                                | 5.37 ms: 1.08x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 106 ns: 1.08x slower                                                     |
| comprehensions             | 16.6 us                                                                | 18.4 us: 1.11x slower                                                    |
| json_loads                 | 27.3 us                                                                | 30.3 us: 1.11x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 6.65 ms: 1.12x slower                                                    |
| async_generators           | 375 ms                                                                 | 421 ms: 1.12x slower                                                     |
| float                      | 76.7 ms                                                                | 86.3 ms: 1.12x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 26.2 ms: 1.13x slower                                                    |
| docutils                   | 2.63 sec                                                               | 2.98 sec: 1.13x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 88.2 ms: 1.13x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.14x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 820 ms: 1.14x slower                                                     |
| logging_simple             | 6.14 us                                                                | 7.06 us: 1.15x slower                                                    |
| logging_format             | 6.92 us                                                                | 7.96 us: 1.15x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 337 us: 1.15x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 22.8 ms: 1.16x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.2 ms: 1.16x slower                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                                   |
| raytrace                   | 250 ms                                                                 | 293 ms: 1.17x slower                                                     |
| 2to3                       | 259 ms                                                                 | 304 ms: 1.17x slower                                                     |
| richards                   | 44.4 ms                                                                | 53.0 ms: 1.19x slower                                                    |
| generators                 | 28.5 ms                                                                | 34.3 ms: 1.20x slower                                                    |
| richards_super             | 50.4 ms                                                                | 60.5 ms: 1.20x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 3.76 ms: 1.21x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                                | 104 ms: 1.21x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.22x slower                                                     |
| thrift                     | 772 us                                                                 | 947 us: 1.23x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 191 ms: 1.24x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.24x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 564 ms: 1.24x slower                                                     |
| django_template            | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 87.6 ms: 1.28x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                                    |
| regex_compile              | 131 ms                                                                 | 172 ms: 1.31x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 77.6 ms: 1.31x slower                                                    |
| nbody                      | 85.3 ms                                                                | 122 ms: 1.43x slower                                                     |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                                    |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                    |
| coverage                   | 82.5 ms                                                                | 120 ms: 1.46x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.37 ms: 1.48x slower                                                    |
| telco                      | 7.77 ms                                                                | 178 ms: 22.88x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                             |

Benchmark hidden because not significant (3): html5lib, async_tree_none_tg, scimark_sparse_mat_mult
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261019-3.16.0a1+dev-2e001e5-NOGIL/bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 93.47% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x