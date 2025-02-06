# Results vs. 3.12.6

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.67 sec: 1.09x faster                                                 |
| html5lib       | 88.9 ms                                                | 78.4 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 914 ms: 2.12x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 902 ms: 2.05x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 473 ms: 1.97x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 501 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 386 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 383 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 699 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 735 ms: 1.47x faster                                                   |
| async_generators           | 589 ms                                                 | 522 ms: 1.13x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 704 ms: 1.06x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.5 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.58x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 114 ms: 1.08x faster                                                   |
| pidigits       | 250 ms                                                 | 232 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                 | 123 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.18 ms: 1.23x faster                                                  |
| regex_compile  | 187 ms                                                 | 157 ms: 1.19x faster                                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 196 ms: 1.23x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.44 sec: 1.18x faster                                                 |
| xml_etree_generate   | 127 ms                                                 | 112 ms: 1.14x faster                                                   |
| pickle_pure_python   | 436 us                                                 | 389 us: 1.12x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 271 us: 1.11x faster                                                   |
| json_dumps           | 14.3 ms                                                | 16.1 ms: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.5 ms: 1.13x faster                                                  |
| python_startup         | 23.7 ms                                                | 26.7 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 28.1 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): django_template, genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 914 ms: 2.12x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 902 ms: 2.05x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 473 ms: 1.97x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 501 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 386 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 383 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 699 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 735 ms: 1.47x faster                                                   |
| deepcopy                   | 468 us                                                 | 340 us: 1.38x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 38.6 us: 1.36x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 162 ms: 1.34x faster                                                   |
| comprehensions             | 27.1 us                                                | 20.7 us: 1.31x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.18 ms: 1.23x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 196 ms: 1.23x faster                                                   |
| spectral_norm              | 156 ms                                                 | 127 ms: 1.22x faster                                                   |
| raytrace                   | 408 ms                                                 | 338 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.38 us: 1.19x faster                                                  |
| regex_compile              | 187 ms                                                 | 157 ms: 1.19x faster                                                   |
| pylint                     | 465 ms                                                 | 393 ms: 1.18x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.44 sec: 1.18x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.60 sec: 1.18x faster                                                 |
| pyflate                    | 727 ms                                                 | 628 ms: 1.16x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 92.7 ms: 1.16x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.55 sec: 1.16x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 84.1 ms: 1.15x faster                                                  |
| logging_format             | 9.59 us                                                | 8.39 us: 1.14x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 112 ms: 1.14x faster                                                   |
| html5lib                   | 88.9 ms                                                | 78.4 ms: 1.13x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 15.5 ms: 1.13x faster                                                  |
| scimark_fft                | 500 ms                                                 | 442 ms: 1.13x faster                                                   |
| async_generators           | 589 ms                                                 | 522 ms: 1.13x faster                                                   |
| go                         | 172 ms                                                 | 153 ms: 1.13x faster                                                   |
| pickle_pure_python         | 436 us                                                 | 389 us: 1.12x faster                                                   |
| pathlib                    | 31.6 ms                                                | 28.2 ms: 1.12x faster                                                  |
| richards_super             | 72.8 ms                                                | 65.1 ms: 1.12x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.55 sec: 1.12x faster                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.04 ms: 1.11x faster                                                  |
| unpickle_pure_python       | 300 us                                                 | 271 us: 1.11x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 68.7 ms: 1.11x faster                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.13 ms: 1.10x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 204 us: 1.10x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.55 us: 1.09x faster                                                  |
| sympy_str                  | 385 ms                                                 | 353 ms: 1.09x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.67 sec: 1.09x faster                                                 |
| logging_silent             | 139 ns                                                 | 128 ns: 1.09x faster                                                   |
| chaos                      | 84.9 ms                                                | 78.3 ms: 1.08x faster                                                  |
| float                      | 123 ms                                                 | 114 ms: 1.08x faster                                                   |
| pidigits                   | 250 ms                                                 | 232 ms: 1.08x faster                                                   |
| scimark_sor                | 167 ms                                                 | 155 ms: 1.08x faster                                                   |
| genshi_text                | 30.2 ms                                                | 28.1 ms: 1.08x faster                                                  |
| scimark_lu                 | 152 ms                                                 | 142 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.86 sec: 1.07x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 704 ms: 1.06x faster                                                   |
| richards                   | 60.3 ms                                                | 56.8 ms: 1.06x faster                                                  |
| meteor_contest             | 146 ms                                                 | 140 ms: 1.05x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.5 ms: 1.03x slower                                                  |
| nbody                      | 119 ms                                                 | 123 ms: 1.04x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 1.88 ms: 1.05x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.18 ms: 1.12x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.1 ms: 1.12x slower                                                  |
| python_startup             | 23.7 ms                                                | 26.7 ms: 1.13x slower                                                  |
| telco                      | 9.59 ms                                                | 10.9 ms: 1.14x slower                                                  |
| coverage                   | 95.4 ms                                                | 119 ms: 1.25x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.83 ms: 1.51x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.81 ms: 1.97x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 97.0 ms: 4.69x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (24): bench_thread_pool, nqueens, sympy_integrate, sqlglot_normalize, xml_etree_process, logging_simple, generators, hexiom, fannkuch, xml_etree_iterparse, pprint_safe_repr, sympy_sum, django_template, regex_dna, genshi_xml, dulwich_log, sympy_expand, deltablue, json, 2to3, sqlalchemy_imperative, regex_v8, mako, json_loads
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x