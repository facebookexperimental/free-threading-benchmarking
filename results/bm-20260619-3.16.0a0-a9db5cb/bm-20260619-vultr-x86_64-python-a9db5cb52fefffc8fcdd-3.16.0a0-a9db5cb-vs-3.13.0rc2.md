# Results vs. 3.13.0rc2

- fork: python
- ref: a9db5cb52fefffc8fcdd
- machine: linux-x86_64
- commit hash: a9db5cb
- commit date: 2026-06-19
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 256 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.40 sec: 1.09x faster                                                |
| html5lib       | 68.6 ms                                                                | 60.0 ms: 1.14x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 716 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 378 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 755 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 557 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 361 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 295 ms: 1.13x faster                                                  |
| async_generators           | 375 ms                                                                 | 336 ms: 1.11x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 188 ms: 1.15x faster                                                  |
| float          | 76.7 ms                                                                | 73.4 ms: 1.05x faster                                                 |
| nbody          | 85.3 ms                                                                | 89.9 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.69 ms: 1.20x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                 |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| regex_compile  | 131 ms                                                                 | 122 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.83 sec: 1.10x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.76 ms: 1.09x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 89.6 ms: 1.05x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 85.9 ms: 1.01x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 60.6 ms: 1.02x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 307 us: 1.05x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.1 ms: 1.03x slower                                                 |
| mako            | 11.2 ms                                                                | 12.4 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.77x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                |
| deepcopy                   | 357 us                                                                 | 232 us: 1.54x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.3 us: 1.45x faster                                                 |
| go                         | 141 ms                                                                 | 102 ms: 1.38x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 118 us: 1.32x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 107 ms: 1.25x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 716 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 378 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.21x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.69 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 755 ms: 1.19x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 92.1 ms: 1.17x faster                                                 |
| pidigits                   | 216 ms                                                                 | 188 ms: 1.15x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 60.0 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 557 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 361 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 295 ms: 1.13x faster                                                  |
| async_generators           | 375 ms                                                                 | 336 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                                 | 404 ms: 1.11x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 67.6 ms: 1.10x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 316 ms: 1.10x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.83 sec: 1.10x faster                                                |
| docutils                   | 2.63 sec                                                               | 2.40 sec: 1.09x faster                                                |
| json_dumps                 | 10.6 ms                                                                | 9.76 ms: 1.09x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| regex_compile              | 131 ms                                                                 | 122 ms: 1.07x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 73.1 ms: 1.06x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.61 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.49 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.22 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.6 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                 |
| chaos                      | 56.3 ms                                                                | 53.7 ms: 1.05x faster                                                 |
| float                      | 76.7 ms                                                                | 73.4 ms: 1.05x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.88 us: 1.05x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.62 us: 1.04x faster                                                 |
| richards                   | 44.4 ms                                                                | 42.6 ms: 1.04x faster                                                 |
| richards_super             | 50.4 ms                                                                | 48.4 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.22 us: 1.02x faster                                                 |
| 2to3                       | 259 ms                                                                 | 256 ms: 1.01x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 373 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                |
| pprint_safe_repr           | 719 ms                                                                 | 714 ms: 1.01x faster                                                  |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 85.9 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.46 sec: 1.01x slower                                                |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                 |
| coverage                   | 82.5 ms                                                                | 83.4 ms: 1.01x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.01x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 460 ms: 1.01x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.4 ms: 1.02x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.09 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 60.6 ms: 1.02x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.18 ms: 1.03x slower                                                 |
| django_template            | 34.2 ms                                                                | 35.1 ms: 1.03x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| nbody                      | 85.3 ms                                                                | 89.9 ms: 1.05x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 307 us: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.4 ms: 1.10x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 3.77 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.68 ms: 1.26x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 158 ms: 20.32x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 248 ms: 22.51x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (5): json_loads, sympy_str, logging_silent, thrift, generators
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x