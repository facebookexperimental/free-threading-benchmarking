# Results vs. 3.12.6

- fork: python
- ref: e66f87ca73516efb4aec
- machine: linux-x86_64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.019x slower
- HPT reliability: 91.04%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                 |
| html5lib       | 63.6 ms                                                | 67.1 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 521 ms: 2.13x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 543 ms: 2.00x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 283 ms: 1.97x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                   |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.05x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 235 us: 1.07x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 31.7 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                  |
| genshi_xml      | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                  |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 521 ms: 2.13x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 543 ms: 2.00x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 283 ms: 1.97x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                 |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.9 us: 1.30x faster                                                  |
| deepcopy                   | 352 us                                                 | 277 us: 1.27x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.05x faster                                                 |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                                  |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.01 us: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.02x faster                                                   |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                   |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                   |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                                   |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.02x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.84 us: 1.03x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.40 ms: 1.04x slower                                                  |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 775 ms: 1.04x slower                                                   |
| html5lib                   | 63.6 ms                                                | 67.1 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.06x slower                                                 |
| logging_format             | 7.35 us                                                | 7.79 us: 1.06x slower                                                  |
| sympy_str                  | 292 ms                                                 | 309 ms: 1.06x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                  |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                   |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 235 us: 1.07x slower                                                   |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.67 ms: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                   |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| nqueens                    | 80.1 ms                                                | 87.1 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                   |
| sympy_expand               | 468 ms                                                 | 516 ms: 1.10x slower                                                   |
| richards                   | 45.9 ms                                                | 51.7 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                  |
| thrift                     | 791 us                                                 | 894 us: 1.13x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                                  |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.14x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 186 us: 1.14x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.14x slower                                                   |
| richards_super             | 51.9 ms                                                | 59.5 ms: 1.15x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                  |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.17x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 80.1 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.7 us: 1.19x slower                                                  |
| fannkuch                   | 372 ms                                                 | 453 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.40 ms: 1.23x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.37x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 15.1 ms: 1.40x slower                                                  |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| coverage                   | 71.4 ms                                                | 110 ms: 1.55x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.05 ms: 3.24x slower                                                  |
| telco                      | 6.53 ms                                                | 176 ms: 26.90x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): scimark_fft
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 91.04% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x