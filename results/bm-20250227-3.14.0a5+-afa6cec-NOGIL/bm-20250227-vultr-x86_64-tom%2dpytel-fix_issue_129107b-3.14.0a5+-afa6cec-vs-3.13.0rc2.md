# Results vs. 3.13.0rc2

- fork: tom-pytel
- ref: fix_issue_129107b
- machine: linux-x86_64
- commit hash: afa6cec
- commit date: 2025-02-27
- overall geometric mean: 1.075x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 305 ms: 1.18x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                   |
| html5lib       | 68.6 ms                                                                | 70.0 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 548 ms: 1.64x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 579 ms: 1.52x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.40x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 338 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 203 ms: 1.07x faster                                                     |
| float          | 76.7 ms                                                                | 76.3 ms: 1.01x faster                                                    |
| nbody          | 85.3 ms                                                                | 134 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                    |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.10x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                    |
| regex_compile  | 131 ms                                                                 | 156 ms: 1.18x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.3 ms: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                     |
| json_loads           | 27.3 us                                                                | 29.1 us: 1.07x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 69.4 ms: 1.17x slower                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.37 sec: 1.18x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                    |
| pickle_pure_python   | 292 us                                                                 | 360 us: 1.24x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.66 ms: 1.30x slower                                                    |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.4 ms: 1.23x slower                                                    |
| django_template | 34.2 ms                                                                | 43.0 ms: 1.26x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 28.4 ms: 1.30x slower                                                    |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 548 ms: 1.64x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 579 ms: 1.52x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.40x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 338 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                    |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.10x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.3 ms: 1.08x faster                                                    |
| pidigits                   | 216 ms                                                                 | 203 ms: 1.07x faster                                                     |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                    |
| go                         | 141 ms                                                                 | 140 ms: 1.01x faster                                                     |
| float                      | 76.7 ms                                                                | 76.3 ms: 1.01x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.02x slower                                                     |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                    |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                    |
| html5lib                   | 68.6 ms                                                                | 70.0 ms: 1.02x slower                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 3.19 us: 1.02x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.03x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                   |
| json_loads                 | 27.3 us                                                                | 29.1 us: 1.07x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.76 sec: 1.07x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 82.5 ms: 1.11x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                    |
| pyflate                    | 449 ms                                                                 | 506 ms: 1.13x slower                                                     |
| logging_silent             | 98.2 ns                                                                | 111 ns: 1.13x slower                                                     |
| telco                      | 7.77 ms                                                                | 8.77 ms: 1.13x slower                                                    |
| thrift                     | 772 us                                                                 | 871 us: 1.13x slower                                                     |
| scimark_fft                | 348 ms                                                                 | 395 ms: 1.14x slower                                                     |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.14x slower                                                     |
| generators                 | 28.5 ms                                                                | 32.9 ms: 1.15x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                                | 61.0 ms: 1.16x slower                                                    |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 842 ms: 1.17x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 69.4 ms: 1.17x slower                                                    |
| logging_simple             | 6.14 us                                                                | 7.22 us: 1.17x slower                                                    |
| 2to3                       | 259 ms                                                                 | 305 ms: 1.18x slower                                                     |
| coverage                   | 82.5 ms                                                                | 97.0 ms: 1.18x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.37 sec: 1.18x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.15 us: 1.18x slower                                                    |
| regex_compile              | 131 ms                                                                 | 156 ms: 1.18x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                                    |
| comprehensions             | 16.6 us                                                                | 20.2 us: 1.22x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 553 ms: 1.22x slower                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.81 ms: 1.22x slower                                                    |
| sqlglot_transpile          | 1.55 ms                                                                | 1.90 ms: 1.22x slower                                                    |
| richards                   | 44.4 ms                                                                | 54.5 ms: 1.23x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.23x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 60.4 ms: 1.23x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 360 us: 1.24x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.84 ms: 1.24x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 7.43 ms: 1.25x slower                                                    |
| chaos                      | 56.3 ms                                                                | 70.6 ms: 1.25x slower                                                    |
| django_template            | 34.2 ms                                                                | 43.0 ms: 1.26x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.27x slower                                                    |
| nqueens                    | 77.7 ms                                                                | 98.9 ms: 1.27x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 144 ms: 1.28x slower                                                     |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.6 ms: 1.29x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 87.8 ms: 1.29x slower                                                    |
| richards_super             | 50.4 ms                                                                | 65.2 ms: 1.29x slower                                                    |
| raytrace                   | 250 ms                                                                 | 324 ms: 1.30x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 9.66 ms: 1.30x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 28.4 ms: 1.30x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 493 ms: 1.31x slower                                                     |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                    |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                    |
| nbody                      | 85.3 ms                                                                | 134 ms: 1.58x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.32 ms: 3.59x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 95.4 ms: 8.68x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                             |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, async_generators, deepcopy_memo
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250227-3.14.0a5+-afa6cec-NOGIL/bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x