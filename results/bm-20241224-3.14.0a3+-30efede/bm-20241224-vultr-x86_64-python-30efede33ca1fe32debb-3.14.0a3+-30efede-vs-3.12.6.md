# Results vs. 3.12.6

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.087x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 610 ms: 1.82x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 634 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 279 ms: 1.67x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                  |
| async_generators           | 384 ms                                                 | 353 ms: 1.09x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| nbody          | 89.3 ms                                                | 90.4 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.4 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 26.3 us: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 311 us: 1.01x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 49.1 ms: 1.02x faster                                                  |
| mako           | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 610 ms: 1.82x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 634 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 279 ms: 1.67x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                   |
| deepcopy                   | 352 us                                                 | 254 us: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.33x faster                                                  |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.17x faster                                                  |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                   |
| spectral_norm              | 110 ms                                                 | 95.8 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.5 ms: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                                   |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.13x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.4 ms: 1.13x faster                                                  |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.97 us: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.62 us: 1.11x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.28 sec: 1.11x faster                                                 |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.09x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.15 ms: 1.09x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.6 ms: 1.09x faster                                                  |
| async_generators           | 384 ms                                                 | 353 ms: 1.09x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 63.1 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 730 us: 1.08x faster                                                   |
| richards                   | 45.9 ms                                                | 42.5 ms: 1.08x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.5 ms: 1.07x faster                                                  |
| scimark_fft                | 342 ms                                                 | 319 ms: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.27 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                  |
| pyflate                    | 448 ms                                                 | 420 ms: 1.07x faster                                                   |
| float                      | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.58 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 705 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.90 ms: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 75.5 ms: 1.04x faster                                                  |
| json                       | 5.02 ms                                                | 4.82 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                   |
| nqueens                    | 80.1 ms                                                | 77.7 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                   |
| fannkuch                   | 372 ms                                                 | 362 ms: 1.03x faster                                                   |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.03x faster                                                   |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.4 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 52.1 ms: 1.02x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.1 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                   |
| logging_silent             | 109 ns                                                 | 107 ns: 1.01x faster                                                   |
| json_loads                 | 26.5 us                                                | 26.3 us: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 311 us: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| nbody                      | 89.3 ms                                                | 90.4 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.46 ms: 1.01x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.46 sec: 1.02x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.9 ms: 1.10x slower                                                  |
| telco                      | 6.53 ms                                                | 7.36 ms: 1.13x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.32 ms: 1.25x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.7 ms: 8.31x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): sqlite_synth, django_template
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x