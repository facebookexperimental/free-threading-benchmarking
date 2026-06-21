# Results vs. 3.13.0rc2

- fork: python
- ref: a9db5cb52fefffc8fcdd
- machine: linux-x86_64
- commit hash: a9db5cb
- commit date: 2026-06-19
- overall geometric mean: 1.069x slower
- HPT reliability: 98.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| html5lib       | 68.6 ms                                                                | 69.0 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 677 ms: 1.33x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 699 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 416 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 578 ms: 1.10x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 337 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 391 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 322 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 386 ms: 1.03x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.6 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 181 ms: 1.19x faster                                                  |
| float          | 76.7 ms                                                                | 86.2 ms: 1.12x slower                                                 |
| nbody          | 85.3 ms                                                                | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                 |
| regex_effbot   | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                 |
| regex_dna      | 189 ms                                                                 | 188 ms: 1.00x faster                                                  |
| regex_compile  | 131 ms                                                                 | 141 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.2 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.3 us: 1.11x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 237 us: 1.14x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 338 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 74.6 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.18 ms: 1.24x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.1 ms: 1.20x slower                                                 |
| mako            | 11.2 ms                                                                | 16.3 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 133 ms: 2.38x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.76 ms: 1.89x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.80x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.86 ms: 1.60x faster                                                 |
| deepcopy                   | 357 us                                                                 | 265 us: 1.35x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 677 ms: 1.33x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 699 ms: 1.26x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 31.1 us: 1.23x faster                                                 |
| pidigits                   | 216 ms                                                                 | 181 ms: 1.19x faster                                                  |
| go                         | 141 ms                                                                 | 120 ms: 1.18x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.96 us: 1.15x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 416 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 578 ms: 1.10x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.6 ms: 1.09x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.87 us: 1.09x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 145 us: 1.07x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 69.9 ms: 1.07x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 337 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 391 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 322 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.02x faster                                                |
| regex_effbot               | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 188 ms: 1.00x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 69.0 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.34 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.2 ms: 1.01x slower                                                 |
| pyflate                    | 449 ms                                                                 | 454 ms: 1.01x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 353 ms: 1.01x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                                  |
| async_generators           | 375 ms                                                                 | 386 ms: 1.03x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.3 us: 1.04x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                |
| coroutines                 | 23.3 ms                                                                | 24.6 ms: 1.05x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 104 ns: 1.06x slower                                                  |
| json                       | 4.98 ms                                                                | 5.30 ms: 1.06x slower                                                 |
| regex_compile              | 131 ms                                                                 | 141 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 797 ms: 1.11x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.3 us: 1.11x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.63 ms: 1.11x slower                                                 |
| generators                 | 28.5 ms                                                                | 31.8 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.12x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.3 ms: 1.12x slower                                                 |
| float                      | 76.7 ms                                                                | 86.2 ms: 1.12x slower                                                 |
| chaos                      | 56.3 ms                                                                | 63.3 ms: 1.12x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.79 us: 1.13x slower                                                 |
| 2to3                       | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| logging_simple             | 6.14 us                                                                | 6.94 us: 1.13x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 237 us: 1.14x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.14x slower                                                |
| sympy_str                  | 274 ms                                                                 | 316 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 338 us: 1.16x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 131 ms: 1.16x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 527 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.54 ms: 1.17x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 182 ms: 1.18x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.66 ms: 1.18x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| richards                   | 44.4 ms                                                                | 52.7 ms: 1.19x slower                                                 |
| thrift                     | 772 us                                                                 | 926 us: 1.20x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 79.0 ms: 1.20x slower                                                 |
| django_template            | 34.2 ms                                                                | 41.1 ms: 1.20x slower                                                 |
| richards_super             | 50.4 ms                                                                | 60.7 ms: 1.20x slower                                                 |
| raytrace                   | 250 ms                                                                 | 306 ms: 1.22x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 464 ms: 1.23x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.18 ms: 1.24x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 74.6 ms: 1.26x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 90.6 ms: 1.33x slower                                                 |
| coverage                   | 82.5 ms                                                                | 114 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| mako                       | 11.2 ms                                                                | 16.3 ms: 1.45x slower                                                 |
| nbody                      | 85.3 ms                                                                | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.47 ms: 1.59x slower                                                 |
| telco                      | 7.77 ms                                                                | 175 ms: 22.48x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): json_dumps
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 98.76% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x