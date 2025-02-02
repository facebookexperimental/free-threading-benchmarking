# Results vs. 3.12.6

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.056x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 562 ms: 1.23x slower                                                   |
| html5lib       | 88.9 ms                                                | 98.6 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 801 ms: 2.41x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 838 ms: 2.20x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 511 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 506 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 383 ms: 1.84x faster                                                   |
| async_tree_none            | 741 ms                                                 | 406 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 648 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 795 ms: 1.36x faster                                                   |
| async_generators           | 589 ms                                                 | 564 ms: 1.04x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 817 ms: 1.09x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.3 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.50 sec: 1.25x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 1.21 sec: 1.31x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 108 ms: 1.14x faster                                                   |
| pidigits       | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| nbody          | 119 ms                                                 | 194 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.48 ms: 1.15x faster                                                  |
| regex_v8       | 32.5 ms                                                | 36.0 ms: 1.11x slower                                                  |
| regex_dna      | 278 ms                                                 | 310 ms: 1.11x slower                                                   |
| regex_compile  | 187 ms                                                 | 211 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.5 us: 1.16x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| pickle               | 16.4 us                                                | 17.4 us: 1.06x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 464 us: 1.07x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.13 sec: 1.09x slower                                                 |
| unpickle_list        | 6.83 us                                                | 7.84 us: 1.15x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 147 ms: 1.16x slower                                                   |
| json_dumps           | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 357 us: 1.19x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 101 ms: 1.21x slower                                                   |
| json_loads           | 37.9 us                                                | 47.2 us: 1.25x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.6 ms: 1.12x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 56.1 ms: 1.25x slower                                                  |
| genshi_text     | 30.2 ms                                                | 38.3 ms: 1.27x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 87.5 ms: 1.29x slower                                                  |
| mako            | 15.7 ms                                                | 23.5 ms: 1.50x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 801 ms: 2.41x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 838 ms: 2.20x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 511 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 506 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 383 ms: 1.84x faster                                                   |
| async_tree_none            | 741 ms                                                 | 406 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 648 ms: 1.70x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.76 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 795 ms: 1.36x faster                                                   |
| deepcopy                   | 468 us                                                 | 403 us: 1.16x faster                                                   |
| pickle_dict                | 52.7 us                                                | 45.5 us: 1.16x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.48 ms: 1.15x faster                                                  |
| float                      | 123 ms                                                 | 108 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.66 sec: 1.08x faster                                                 |
| async_generators           | 589 ms                                                 | 564 ms: 1.04x faster                                                   |
| pidigits                   | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 4.06 us: 1.05x slower                                                  |
| comprehensions             | 27.1 us                                                | 28.6 us: 1.05x slower                                                  |
| mdp                        | 3.97 sec                                               | 4.21 sec: 1.06x slower                                                 |
| pickle                     | 16.4 us                                                | 17.4 us: 1.06x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 464 us: 1.07x slower                                                   |
| generators                 | 41.1 ms                                                | 44.0 ms: 1.07x slower                                                  |
| scimark_fft                | 500 ms                                                 | 536 ms: 1.07x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 235 ms: 1.08x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.13 sec: 1.09x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.38 us: 1.09x slower                                                  |
| go                         | 172 ms                                                 | 187 ms: 1.09x slower                                                   |
| asyncio_websockets         | 748 ms                                                 | 817 ms: 1.09x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 173 ms: 1.10x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 36.0 ms: 1.11x slower                                                  |
| html5lib                   | 88.9 ms                                                | 98.6 ms: 1.11x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 246 ms: 1.11x slower                                                   |
| deepcopy_memo              | 52.4 us                                                | 58.3 us: 1.11x slower                                                  |
| regex_dna                  | 278 ms                                                 | 310 ms: 1.11x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.6 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.08 sec: 1.12x slower                                                 |
| regex_compile              | 187 ms                                                 | 211 ms: 1.13x slower                                                   |
| logging_silent             | 139 ns                                                 | 158 ns: 1.13x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 110 ms: 1.14x slower                                                   |
| unpickle_list              | 6.83 us                                                | 7.84 us: 1.15x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.57 sec: 1.15x slower                                                 |
| xml_etree_generate         | 127 ms                                                 | 147 ms: 1.16x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.3 ms: 1.16x slower                                                  |
| nqueens                    | 117 ms                                                 | 136 ms: 1.17x slower                                                   |
| json                       | 6.85 ms                                                | 8.00 ms: 1.17x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.32 sec: 1.17x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                  |
| raytrace                   | 408 ms                                                 | 480 ms: 1.18x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 180 ms: 1.18x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 128 ms: 1.19x slower                                                   |
| scimark_sor                | 167 ms                                                 | 198 ms: 1.19x slower                                                   |
| richards_super             | 72.8 ms                                                | 86.8 ms: 1.19x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 357 us: 1.19x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 101 ms: 1.21x slower                                                   |
| unpack_sequence            | 60.2 ns                                                | 73.1 ns: 1.21x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 36.2 ms: 1.22x slower                                                  |
| fannkuch                   | 540 ms                                                 | 660 ms: 1.22x slower                                                   |
| 2to3                       | 456 ms                                                 | 562 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.26 ms: 1.23x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.90 ms: 1.24x slower                                                  |
| json_loads                 | 37.9 us                                                | 47.2 us: 1.25x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.50 sec: 1.25x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 30.8 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 280 us: 1.25x slower                                                   |
| meteor_contest             | 146 ms                                                 | 183 ms: 1.25x slower                                                   |
| django_template            | 44.9 ms                                                | 56.1 ms: 1.25x slower                                                  |
| telco                      | 9.59 ms                                                | 12.0 ms: 1.25x slower                                                  |
| sympy_str                  | 385 ms                                                 | 483 ms: 1.25x slower                                                   |
| richards                   | 60.3 ms                                                | 76.4 ms: 1.27x slower                                                  |
| genshi_text                | 30.2 ms                                                | 38.3 ms: 1.27x slower                                                  |
| chaos                      | 84.9 ms                                                | 108 ms: 1.27x slower                                                   |
| sympy_expand               | 582 ms                                                 | 741 ms: 1.27x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 97.0 ms: 1.28x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.49 ms: 1.29x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 87.5 ms: 1.29x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.8 ms: 1.30x slower                                                  |
| asyncio_tcp                | 923 ms                                                 | 1.21 sec: 1.31x slower                                                 |
| logging_format             | 9.59 us                                                | 12.6 us: 1.31x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.6 ms: 1.33x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.45 ms: 1.37x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.55 ms: 1.43x slower                                                  |
| coverage                   | 95.4 ms                                                | 143 ms: 1.49x slower                                                   |
| mako                       | 15.7 ms                                                | 23.5 ms: 1.50x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.04 ms: 1.57x slower                                                  |
| nbody                      | 119 ms                                                 | 194 ms: 1.63x slower                                                   |
| deltablue                  | 4.27 ms                                                | 7.02 ms: 1.65x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 85.5 ms: 4.13x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (10): xml_etree_parse, logging_simple, unpickle, dulwich_log, spectral_norm, docutils, pyflate, pathlib, pickle_list, pylint
Ignored benchmarks (7) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
Ignored benchmarks (6) of results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.056x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x