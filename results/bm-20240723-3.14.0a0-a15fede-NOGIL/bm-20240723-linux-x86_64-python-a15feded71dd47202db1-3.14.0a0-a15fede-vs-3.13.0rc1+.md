# Results vs. 3.13.0rc1+

- fork: python
- ref: a15feded71dd47202db1
- machine: linux-x86_64
- commit hash: a15fede
- commit date: 2024-07-23
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 650 ms: 1.47x slower                                                  |
| docutils       | 4.01 sec                                                | 4.88 sec: 1.22x slower                                                |
| html5lib       | 98.1 ms                                                 | 139 ms: 1.42x slower                                                  |
| tornado_http   | 248 ms                                                  | 349 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                   | 1.38x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.16 sec: 1.25x faster                                                |
| async_tree_none_tg         | 521 ms                                                  | 485 ms: 1.07x faster                                                  |
| async_tree_io              | 1.38 sec                                                | 1.30 sec: 1.06x faster                                                |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 817 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 944 ms: 1.05x slower                                                  |
| asyncio_tcp                | 985 ms                                                  | 1.12 sec: 1.13x slower                                                |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.36 sec: 1.20x slower                                                |
| async_generators           | 592 ms                                                  | 739 ms: 1.25x slower                                                  |
| coroutines                 | 29.2 ms                                                 | 43.2 ms: 1.48x slower                                                 |
| Geometric mean             | (ref)                                                   | 1.04x slower                                                          |

Benchmark hidden because not significant (4): async_tree_memoization, asyncio_websockets, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                  | 202 ms: 1.76x slower                                                  |
| nbody          | 124 ms                                                  | 288 ms: 2.32x slower                                                  |
| Geometric mean | (ref)                                                   | 1.59x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.57 ms: 1.06x faster                                                 |
| regex_v8       | 32.4 ms                                                 | 36.3 ms: 1.12x slower                                                 |
| regex_compile  | 177 ms                                                  | 291 ms: 1.64x slower                                                  |
| Geometric mean | (ref)                                                   | 1.15x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                 | 42.5 us: 1.10x faster                                                 |
| pickle_list          | 6.82 us                                                 | 6.30 us: 1.08x faster                                                 |
| pickle               | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| json_loads           | 36.1 us                                                 | 42.7 us: 1.18x slower                                                 |
| unpickle_list        | 6.67 us                                                 | 8.14 us: 1.22x slower                                                 |
| xml_etree_generate   | 129 ms                                                  | 162 ms: 1.26x slower                                                  |
| json_dumps           | 14.9 ms                                                 | 19.0 ms: 1.28x slower                                                 |
| xml_etree_process    | 86.5 ms                                                 | 127 ms: 1.46x slower                                                  |
| tomli_loads          | 2.80 sec                                                | 4.22 sec: 1.51x slower                                                |
| pickle_pure_python   | 417 us                                                  | 805 us: 1.93x slower                                                  |
| unpickle_pure_python | 296 us                                                  | 609 us: 2.06x slower                                                  |
| Geometric mean       | (ref)                                                   | 1.22x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 29.7 ms: 1.35x slower                                                 |
| python_startup_no_site | 14.6 ms                                                 | 20.6 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 116 ms: 1.69x slower                                                  |
| django_template | 46.9 ms                                                 | 80.4 ms: 1.71x slower                                                 |
| genshi_text     | 31.7 ms                                                 | 54.9 ms: 1.73x slower                                                 |
| mako            | 16.1 ms                                                 | 30.4 ms: 1.89x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.76x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool              | 19.4 ms                                                 | 13.4 ms: 1.44x faster                                                 |
| create_gc_cycles           | 2.46 ms                                                 | 1.94 ms: 1.27x faster                                                 |
| async_tree_io_tg           | 1.46 sec                                                | 1.16 sec: 1.25x faster                                                |
| gc_traversal               | 5.91 ms                                                 | 4.76 ms: 1.24x faster                                                 |
| pickle_dict                | 46.5 us                                                 | 42.5 us: 1.10x faster                                                 |
| pickle_list                | 6.82 us                                                 | 6.30 us: 1.08x faster                                                 |
| async_tree_none_tg         | 521 ms                                                  | 485 ms: 1.07x faster                                                  |
| async_tree_io              | 1.38 sec                                                | 1.30 sec: 1.06x faster                                                |
| regex_effbot               | 4.84 ms                                                 | 4.57 ms: 1.06x faster                                                 |
| pickle                     | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 817 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 944 ms: 1.05x slower                                                  |
| sqlite_synth               | 4.07 us                                                 | 4.35 us: 1.07x slower                                                 |
| regex_v8                   | 32.4 ms                                                 | 36.3 ms: 1.12x slower                                                 |
| asyncio_tcp                | 985 ms                                                  | 1.12 sec: 1.13x slower                                                |
| telco                      | 11.4 ms                                                 | 13.2 ms: 1.16x slower                                                 |
| json_loads                 | 36.1 us                                                 | 42.7 us: 1.18x slower                                                 |
| pathlib                    | 29.3 ms                                                 | 34.8 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.36 sec: 1.20x slower                                                |
| docutils                   | 4.01 sec                                                | 4.88 sec: 1.22x slower                                                |
| json                       | 6.55 ms                                                 | 7.98 ms: 1.22x slower                                                 |
| unpickle_list              | 6.67 us                                                 | 8.14 us: 1.22x slower                                                 |
| async_generators           | 592 ms                                                  | 739 ms: 1.25x slower                                                  |
| meteor_contest             | 157 ms                                                  | 196 ms: 1.25x slower                                                  |
| deepcopy                   | 484 us                                                  | 606 us: 1.25x slower                                                  |
| xml_etree_generate         | 129 ms                                                  | 162 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 8.89 ms: 1.27x slower                                                 |
| json_dumps                 | 14.9 ms                                                 | 19.0 ms: 1.28x slower                                                 |
| pylint                     | 472 ms                                                  | 607 ms: 1.29x slower                                                  |
| bench_thread_pool          | 3.06 ms                                                 | 4.01 ms: 1.31x slower                                                 |
| scimark_fft                | 477 ms                                                  | 633 ms: 1.33x slower                                                  |
| python_startup             | 22.0 ms                                                 | 29.7 ms: 1.35x slower                                                 |
| mdp                        | 3.80 sec                                                | 5.14 sec: 1.35x slower                                                |
| coverage                   | 110 ms                                                  | 150 ms: 1.36x slower                                                  |
| python_startup_no_site     | 14.6 ms                                                 | 20.6 ms: 1.40x slower                                                 |
| tornado_http               | 248 ms                                                  | 349 ms: 1.41x slower                                                  |
| deepcopy_reduce            | 4.27 us                                                 | 6.01 us: 1.41x slower                                                 |
| deepcopy_memo              | 51.7 us                                                 | 72.8 us: 1.41x slower                                                 |
| html5lib                   | 98.1 ms                                                 | 139 ms: 1.42x slower                                                  |
| pycparser                  | 1.57 sec                                                | 2.28 sec: 1.45x slower                                                |
| nqueens                    | 108 ms                                                  | 157 ms: 1.46x slower                                                  |
| sympy_integrate            | 29.7 ms                                                 | 43.3 ms: 1.46x slower                                                 |
| xml_etree_process          | 86.5 ms                                                 | 127 ms: 1.46x slower                                                  |
| dulwich_log                | 100.0 ms                                                | 146 ms: 1.46x slower                                                  |
| 2to3                       | 442 ms                                                  | 650 ms: 1.47x slower                                                  |
| coroutines                 | 29.2 ms                                                 | 43.2 ms: 1.48x slower                                                 |
| generators                 | 39.2 ms                                                 | 58.0 ms: 1.48x slower                                                 |
| fannkuch                   | 543 ms                                                  | 808 ms: 1.49x slower                                                  |
| tomli_loads                | 2.80 sec                                                | 4.22 sec: 1.51x slower                                                |
| spectral_norm              | 159 ms                                                  | 246 ms: 1.55x slower                                                  |
| crypto_pyaes               | 99.8 ms                                                 | 155 ms: 1.55x slower                                                  |
| thrift                     | 1.11 ms                                                 | 1.74 ms: 1.56x slower                                                 |
| typing_runtime_protocols   | 216 us                                                  | 339 us: 1.57x slower                                                  |
| sqlglot_normalize          | 146 ms                                                  | 238 ms: 1.63x slower                                                  |
| regex_compile              | 177 ms                                                  | 291 ms: 1.64x slower                                                  |
| bpe_tokeniser              | 6.25 sec                                                | 10.3 sec: 1.66x slower                                                |
| sqlglot_optimize           | 76.2 ms                                                 | 128 ms: 1.68x slower                                                  |
| genshi_xml                 | 68.3 ms                                                 | 116 ms: 1.69x slower                                                  |
| logging_simple             | 8.98 us                                                 | 15.3 us: 1.70x slower                                                 |
| pyflate                    | 661 ms                                                  | 1.13 sec: 1.71x slower                                                |
| django_template            | 46.9 ms                                                 | 80.4 ms: 1.71x slower                                                 |
| genshi_text                | 31.7 ms                                                 | 54.9 ms: 1.73x slower                                                 |
| richards                   | 65.8 ms                                                 | 115 ms: 1.75x slower                                                  |
| float                      | 115 ms                                                  | 202 ms: 1.76x slower                                                  |
| pprint_safe_repr           | 959 ms                                                  | 1.71 sec: 1.78x slower                                                |
| richards_super             | 76.3 ms                                                 | 136 ms: 1.78x slower                                                  |
| pprint_pformat             | 2.00 sec                                                | 3.58 sec: 1.79x slower                                                |
| sympy_str                  | 367 ms                                                  | 667 ms: 1.82x slower                                                  |
| logging_format             | 9.48 us                                                 | 17.3 us: 1.82x slower                                                 |
| comprehensions             | 20.9 us                                                 | 39.2 us: 1.87x slower                                                 |
| mako                       | 16.1 ms                                                 | 30.4 ms: 1.89x slower                                                 |
| scimark_monte_carlo        | 89.9 ms                                                 | 171 ms: 1.91x slower                                                  |
| logging_silent             | 130 ns                                                  | 251 ns: 1.93x slower                                                  |
| pickle_pure_python         | 417 us                                                  | 805 us: 1.93x slower                                                  |
| hexiom                     | 8.35 ms                                                 | 16.2 ms: 1.93x slower                                                 |
| scimark_sor                | 172 ms                                                  | 341 ms: 1.98x slower                                                  |
| sympy_expand               | 631 ms                                                  | 1.25 sec: 1.99x slower                                                |
| unpickle_pure_python       | 296 us                                                  | 609 us: 2.06x slower                                                  |
| chaos                      | 84.7 ms                                                 | 175 ms: 2.06x slower                                                  |
| sqlglot_transpile          | 2.30 ms                                                 | 4.92 ms: 2.14x slower                                                 |
| go                         | 195 ms                                                  | 421 ms: 2.15x slower                                                  |
| scimark_lu                 | 154 ms                                                  | 332 ms: 2.16x slower                                                  |
| sqlglot_parse              | 1.80 ms                                                 | 3.96 ms: 2.20x slower                                                 |
| sympy_sum                  | 213 ms                                                  | 477 ms: 2.24x slower                                                  |
| raytrace                   | 350 ms                                                  | 802 ms: 2.29x slower                                                  |
| nbody                      | 124 ms                                                  | 288 ms: 2.32x slower                                                  |
| deltablue                  | 4.56 ms                                                 | 11.7 ms: 2.56x slower                                                 |
| unpack_sequence            | 73.9 ns                                                 | 210 ns: 2.84x slower                                                  |
| Geometric mean             | (ref)                                                   | 1.41x slower                                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, async_tree_memoization, asyncio_websockets, xml_etree_parse, pidigits, async_tree_memoization_tg, async_tree_none, regex_dna, unpickle
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x