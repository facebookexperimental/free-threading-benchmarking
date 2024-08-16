# Results vs. 3.13.0rc1+

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 651 ms: 1.47x slower                                                  |
| docutils       | 4.01 sec                                                | 4.92 sec: 1.23x slower                                                |
| html5lib       | 98.1 ms                                                 | 137 ms: 1.39x slower                                                  |
| tornado_http   | 248 ms                                                  | 319 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                   | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|---------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 1.46 sec                                                | 1.12 sec: 1.30x faster                                                |
| async_tree_io             | 1.38 sec                                                | 1.25 sec: 1.10x faster                                                |
| async_tree_memoization_tg | 672 ms                                                  | 619 ms: 1.09x faster                                                  |
| async_tree_none_tg        | 521 ms                                                  | 489 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 951 ms: 1.06x slower                                                  |
| asyncio_tcp               | 985 ms                                                  | 1.09 sec: 1.11x slower                                                |
| asyncio_tcp_ssl           | 2.79 sec                                                | 3.34 sec: 1.20x slower                                                |
| async_generators          | 592 ms                                                  | 747 ms: 1.26x slower                                                  |
| coroutines                | 29.2 ms                                                 | 42.7 ms: 1.46x slower                                                 |
| Geometric mean            | (ref)                                                   | 1.04x slower                                                          |

Benchmark hidden because not significant (4): async_tree_memoization, asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 248 ms                                                  | 239 ms: 1.04x faster                                                  |
| float          | 115 ms                                                  | 194 ms: 1.69x slower                                                  |
| nbody          | 124 ms                                                  | 281 ms: 2.27x slower                                                  |
| Geometric mean | (ref)                                                   | 1.55x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 35.6 ms: 1.10x slower                                                 |
| regex_compile  | 177 ms                                                  | 296 ms: 1.67x slower                                                  |
| Geometric mean | (ref)                                                   | 1.17x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 218 ms: 1.08x faster                                                  |
| pickle_dict          | 46.5 us                                                 | 43.1 us: 1.08x faster                                                 |
| pickle               | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| json_loads           | 36.1 us                                                 | 41.2 us: 1.14x slower                                                 |
| unpickle_list        | 6.67 us                                                 | 7.70 us: 1.16x slower                                                 |
| json_dumps           | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                                 |
| xml_etree_generate   | 129 ms                                                  | 159 ms: 1.23x slower                                                  |
| xml_etree_process    | 86.5 ms                                                 | 127 ms: 1.47x slower                                                  |
| tomli_loads          | 2.80 sec                                                | 4.14 sec: 1.48x slower                                                |
| unpickle_pure_python | 296 us                                                  | 544 us: 1.84x slower                                                  |
| pickle_pure_python   | 417 us                                                  | 846 us: 2.03x slower                                                  |
| Geometric mean       | (ref)                                                   | 1.20x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 28.9 ms: 1.31x slower                                                 |
| python_startup_no_site | 14.6 ms                                                 | 19.4 ms: 1.32x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 111 ms: 1.63x slower                                                  |
| genshi_text     | 31.7 ms                                                 | 53.4 ms: 1.68x slower                                                 |
| django_template | 46.9 ms                                                 | 79.6 ms: 1.70x slower                                                 |
| mako            | 16.1 ms                                                 | 31.0 ms: 1.93x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.73x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|---------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal              | 5.91 ms                                                 | 4.19 ms: 1.41x faster                                                 |
| create_gc_cycles          | 2.46 ms                                                 | 1.80 ms: 1.37x faster                                                 |
| async_tree_io_tg          | 1.46 sec                                                | 1.12 sec: 1.30x faster                                                |
| async_tree_io             | 1.38 sec                                                | 1.25 sec: 1.10x faster                                                |
| async_tree_memoization_tg | 672 ms                                                  | 619 ms: 1.09x faster                                                  |
| xml_etree_parse           | 236 ms                                                  | 218 ms: 1.08x faster                                                  |
| pickle_dict               | 46.5 us                                                 | 43.1 us: 1.08x faster                                                 |
| async_tree_none_tg        | 521 ms                                                  | 489 ms: 1.07x faster                                                  |
| pickle                    | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| pidigits                  | 248 ms                                                  | 239 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 951 ms: 1.06x slower                                                  |
| sqlite_synth              | 4.07 us                                                 | 4.42 us: 1.08x slower                                                 |
| regex_v8                  | 32.4 ms                                                 | 35.6 ms: 1.10x slower                                                 |
| asyncio_tcp               | 985 ms                                                  | 1.09 sec: 1.11x slower                                                |
| pathlib                   | 29.3 ms                                                 | 33.0 ms: 1.13x slower                                                 |
| json_loads                | 36.1 us                                                 | 41.2 us: 1.14x slower                                                 |
| unpickle_list             | 6.67 us                                                 | 7.70 us: 1.16x slower                                                 |
| deepcopy                  | 484 us                                                  | 560 us: 1.16x slower                                                  |
| asyncio_tcp_ssl           | 2.79 sec                                                | 3.34 sec: 1.20x slower                                                |
| json_dumps                | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                                 |
| meteor_contest            | 157 ms                                                  | 192 ms: 1.23x slower                                                  |
| pylint                    | 472 ms                                                  | 579 ms: 1.23x slower                                                  |
| telco                     | 11.4 ms                                                 | 14.0 ms: 1.23x slower                                                 |
| docutils                  | 4.01 sec                                                | 4.92 sec: 1.23x slower                                                |
| xml_etree_generate        | 129 ms                                                  | 159 ms: 1.23x slower                                                  |
| json                      | 6.55 ms                                                 | 8.10 ms: 1.24x slower                                                 |
| async_generators          | 592 ms                                                  | 747 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult   | 6.98 ms                                                 | 8.91 ms: 1.28x slower                                                 |
| tornado_http              | 248 ms                                                  | 319 ms: 1.28x slower                                                  |
| deepcopy_memo             | 51.7 us                                                 | 67.1 us: 1.30x slower                                                 |
| python_startup            | 22.0 ms                                                 | 28.9 ms: 1.31x slower                                                 |
| scimark_fft               | 477 ms                                                  | 624 ms: 1.31x slower                                                  |
| python_startup_no_site    | 14.6 ms                                                 | 19.4 ms: 1.32x slower                                                 |
| coverage                  | 110 ms                                                  | 146 ms: 1.33x slower                                                  |
| deepcopy_reduce           | 4.27 us                                                 | 5.70 us: 1.34x slower                                                 |
| mdp                       | 3.80 sec                                                | 5.13 sec: 1.35x slower                                                |
| html5lib                  | 98.1 ms                                                 | 137 ms: 1.39x slower                                                  |
| fannkuch                  | 543 ms                                                  | 762 ms: 1.40x slower                                                  |
| generators                | 39.2 ms                                                 | 55.0 ms: 1.40x slower                                                 |
| pycparser                 | 1.57 sec                                                | 2.21 sec: 1.41x slower                                                |
| nqueens                   | 108 ms                                                  | 155 ms: 1.43x slower                                                  |
| coroutines                | 29.2 ms                                                 | 42.7 ms: 1.46x slower                                                 |
| xml_etree_process         | 86.5 ms                                                 | 127 ms: 1.47x slower                                                  |
| 2to3                      | 442 ms                                                  | 651 ms: 1.47x slower                                                  |
| bench_thread_pool         | 3.06 ms                                                 | 4.52 ms: 1.48x slower                                                 |
| tomli_loads               | 2.80 sec                                                | 4.14 sec: 1.48x slower                                                |
| thrift                    | 1.11 ms                                                 | 1.67 ms: 1.50x slower                                                 |
| richards                  | 65.8 ms                                                 | 99.2 ms: 1.51x slower                                                 |
| typing_runtime_protocols  | 216 us                                                  | 327 us: 1.51x slower                                                  |
| sympy_integrate           | 29.7 ms                                                 | 44.9 ms: 1.52x slower                                                 |
| spectral_norm             | 159 ms                                                  | 247 ms: 1.55x slower                                                  |
| crypto_pyaes              | 99.8 ms                                                 | 156 ms: 1.56x slower                                                  |
| sqlglot_normalize         | 146 ms                                                  | 229 ms: 1.57x slower                                                  |
| sqlglot_optimize          | 76.2 ms                                                 | 121 ms: 1.59x slower                                                  |
| pyflate                   | 661 ms                                                  | 1.07 sec: 1.61x slower                                                |
| bpe_tokeniser             | 6.25 sec                                                | 10.1 sec: 1.62x slower                                                |
| genshi_xml                | 68.3 ms                                                 | 111 ms: 1.63x slower                                                  |
| richards_super            | 76.3 ms                                                 | 127 ms: 1.66x slower                                                  |
| regex_compile             | 177 ms                                                  | 296 ms: 1.67x slower                                                  |
| genshi_text               | 31.7 ms                                                 | 53.4 ms: 1.68x slower                                                 |
| float                     | 115 ms                                                  | 194 ms: 1.69x slower                                                  |
| pprint_pformat            | 2.00 sec                                                | 3.39 sec: 1.70x slower                                                |
| django_template           | 46.9 ms                                                 | 79.6 ms: 1.70x slower                                                 |
| logging_simple            | 8.98 us                                                 | 15.4 us: 1.71x slower                                                 |
| pprint_safe_repr          | 959 ms                                                  | 1.65 sec: 1.72x slower                                                |
| logging_format            | 9.48 us                                                 | 16.4 us: 1.73x slower                                                 |
| scimark_monte_carlo       | 89.9 ms                                                 | 159 ms: 1.77x slower                                                  |
| sympy_str                 | 367 ms                                                  | 675 ms: 1.84x slower                                                  |
| unpickle_pure_python      | 296 us                                                  | 544 us: 1.84x slower                                                  |
| comprehensions            | 20.9 us                                                 | 38.7 us: 1.85x slower                                                 |
| sqlglot_transpile         | 2.30 ms                                                 | 4.32 ms: 1.88x slower                                                 |
| logging_silent            | 130 ns                                                  | 249 ns: 1.92x slower                                                  |
| mako                      | 16.1 ms                                                 | 31.0 ms: 1.93x slower                                                 |
| hexiom                    | 8.35 ms                                                 | 16.3 ms: 1.95x slower                                                 |
| scimark_sor               | 172 ms                                                  | 340 ms: 1.97x slower                                                  |
| chaos                     | 84.7 ms                                                 | 170 ms: 2.01x slower                                                  |
| pickle_pure_python        | 417 us                                                  | 846 us: 2.03x slower                                                  |
| scimark_lu                | 154 ms                                                  | 313 ms: 2.03x slower                                                  |
| sympy_expand              | 631 ms                                                  | 1.29 sec: 2.04x slower                                                |
| sympy_sum                 | 213 ms                                                  | 443 ms: 2.08x slower                                                  |
| sqlglot_parse             | 1.80 ms                                                 | 3.76 ms: 2.09x slower                                                 |
| go                        | 195 ms                                                  | 434 ms: 2.22x slower                                                  |
| nbody                     | 124 ms                                                  | 281 ms: 2.27x slower                                                  |
| raytrace                  | 350 ms                                                  | 801 ms: 2.29x slower                                                  |
| deltablue                 | 4.56 ms                                                 | 11.6 ms: 2.54x slower                                                 |
| unpack_sequence           | 73.9 ns                                                 | 190 ns: 2.57x slower                                                  |
| Geometric mean            | (ref)                                                   | 1.39x slower                                                          |

Benchmark hidden because not significant (10): xml_etree_iterparse, bench_mp_pool, async_tree_memoization, asyncio_websockets, regex_effbot, regex_dna, pickle_list, async_tree_none, async_tree_cpu_io_mixed_tg, unpickle
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x