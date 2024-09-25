# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 661 ms: 1.49x slower                                  |
| docutils       | 4.01 sec                                                | 5.15 sec: 1.29x slower                                |
| html5lib       | 98.1 ms                                                 | 145 ms: 1.47x slower                                  |
| tornado_http   | 248 ms                                                  | 360 ms: 1.45x slower                                  |
| Geometric mean | (ref)                                                   | 1.42x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| async_tree_io           | 1.38 sec                                                | 1.30 sec: 1.06x faster                                |
| async_tree_cpu_io_mixed | 899 ms                                                  | 945 ms: 1.05x slower                                  |
| async_tree_memoization  | 745 ms                                                  | 787 ms: 1.06x slower                                  |
| async_tree_none         | 576 ms                                                  | 621 ms: 1.08x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.17 sec: 1.18x slower                                |
| async_generators        | 592 ms                                                  | 744 ms: 1.26x slower                                  |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.55 sec: 1.27x slower                                |
| coroutines              | 29.2 ms                                                 | 44.5 ms: 1.52x slower                                 |
| Geometric mean          | (ref)                                                   | 1.08x slower                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                  | 206 ms: 1.79x slower                                  |
| nbody          | 124 ms                                                  | 293 ms: 2.36x slower                                  |
| Geometric mean | (ref)                                                   | 1.61x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.62 ms: 1.05x faster                                 |
| regex_v8       | 32.4 ms                                                 | 36.7 ms: 1.13x slower                                 |
| regex_compile  | 177 ms                                                  | 290 ms: 1.64x slower                                  |
| Geometric mean | (ref)                                                   | 1.15x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 6.82 us                                                 | 6.17 us: 1.11x faster                                 |
| xml_etree_parse      | 236 ms                                                  | 223 ms: 1.06x faster                                  |
| pickle               | 15.4 us                                                 | 14.6 us: 1.05x faster                                 |
| json_loads           | 36.1 us                                                 | 43.2 us: 1.20x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 159 ms: 1.23x slower                                  |
| unpickle_list        | 6.67 us                                                 | 8.50 us: 1.28x slower                                 |
| json_dumps           | 14.9 ms                                                 | 19.1 ms: 1.28x slower                                 |
| tomli_loads          | 2.80 sec                                                | 4.26 sec: 1.52x slower                                |
| xml_etree_process    | 86.5 ms                                                 | 137 ms: 1.58x slower                                  |
| pickle_pure_python   | 417 us                                                  | 803 us: 1.93x slower                                  |
| unpickle_pure_python | 296 us                                                  | 619 us: 2.09x slower                                  |
| Geometric mean       | (ref)                                                   | 1.23x slower                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 31.5 ms: 1.43x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 21.2 ms: 1.45x slower                                 |
| Geometric mean         | (ref)                                                   | 1.44x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 117 ms: 1.71x slower                                  |
| genshi_text     | 31.7 ms                                                 | 55.9 ms: 1.76x slower                                 |
| django_template | 46.9 ms                                                 | 85.9 ms: 1.83x slower                                 |
| mako            | 16.1 ms                                                 | 32.0 ms: 1.99x slower                                 |
| Geometric mean  | (ref)                                                   | 1.82x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg         | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| create_gc_cycles         | 2.46 ms                                                 | 2.01 ms: 1.22x faster                                 |
| bench_mp_pool            | 19.4 ms                                                 | 16.8 ms: 1.15x faster                                 |
| pickle_list              | 6.82 us                                                 | 6.17 us: 1.11x faster                                 |
| gc_traversal             | 5.91 ms                                                 | 5.42 ms: 1.09x faster                                 |
| xml_etree_parse          | 236 ms                                                  | 223 ms: 1.06x faster                                  |
| async_tree_io            | 1.38 sec                                                | 1.30 sec: 1.06x faster                                |
| pickle                   | 15.4 us                                                 | 14.6 us: 1.05x faster                                 |
| regex_effbot             | 4.84 ms                                                 | 4.62 ms: 1.05x faster                                 |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 945 ms: 1.05x slower                                  |
| async_tree_memoization   | 745 ms                                                  | 787 ms: 1.06x slower                                  |
| sqlite_synth             | 4.07 us                                                 | 4.38 us: 1.08x slower                                 |
| async_tree_none          | 576 ms                                                  | 621 ms: 1.08x slower                                  |
| regex_v8                 | 32.4 ms                                                 | 36.7 ms: 1.13x slower                                 |
| pathlib                  | 29.3 ms                                                 | 34.5 ms: 1.18x slower                                 |
| deepcopy                 | 484 us                                                  | 571 us: 1.18x slower                                  |
| asyncio_tcp              | 985 ms                                                  | 1.17 sec: 1.18x slower                                |
| json_loads               | 36.1 us                                                 | 43.2 us: 1.20x slower                                 |
| xml_etree_generate       | 129 ms                                                  | 159 ms: 1.23x slower                                  |
| pylint                   | 472 ms                                                  | 588 ms: 1.25x slower                                  |
| async_generators         | 592 ms                                                  | 744 ms: 1.26x slower                                  |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.55 sec: 1.27x slower                                |
| unpickle_list            | 6.67 us                                                 | 8.50 us: 1.28x slower                                 |
| json_dumps               | 14.9 ms                                                 | 19.1 ms: 1.28x slower                                 |
| docutils                 | 4.01 sec                                                | 5.15 sec: 1.29x slower                                |
| telco                    | 11.4 ms                                                 | 14.8 ms: 1.29x slower                                 |
| json                     | 6.55 ms                                                 | 8.55 ms: 1.31x slower                                 |
| scimark_fft              | 477 ms                                                  | 628 ms: 1.32x slower                                  |
| coverage                 | 110 ms                                                  | 146 ms: 1.32x slower                                  |
| meteor_contest           | 157 ms                                                  | 210 ms: 1.34x slower                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 9.62 ms: 1.38x slower                                 |
| mdp                      | 3.80 sec                                                | 5.24 sec: 1.38x slower                                |
| pycparser                | 1.57 sec                                                | 2.18 sec: 1.39x slower                                |
| deepcopy_memo            | 51.7 us                                                 | 72.7 us: 1.41x slower                                 |
| python_startup           | 22.0 ms                                                 | 31.5 ms: 1.43x slower                                 |
| deepcopy_reduce          | 4.27 us                                                 | 6.14 us: 1.44x slower                                 |
| python_startup_no_site   | 14.6 ms                                                 | 21.2 ms: 1.45x slower                                 |
| tornado_http             | 248 ms                                                  | 360 ms: 1.45x slower                                  |
| html5lib                 | 98.1 ms                                                 | 145 ms: 1.47x slower                                  |
| fannkuch                 | 543 ms                                                  | 804 ms: 1.48x slower                                  |
| generators               | 39.2 ms                                                 | 58.3 ms: 1.49x slower                                 |
| 2to3                     | 442 ms                                                  | 661 ms: 1.49x slower                                  |
| tomli_loads              | 2.80 sec                                                | 4.26 sec: 1.52x slower                                |
| coroutines               | 29.2 ms                                                 | 44.5 ms: 1.52x slower                                 |
| thrift                   | 1.11 ms                                                 | 1.72 ms: 1.55x slower                                 |
| crypto_pyaes             | 99.8 ms                                                 | 157 ms: 1.57x slower                                  |
| nqueens                  | 108 ms                                                  | 170 ms: 1.58x slower                                  |
| bench_thread_pool        | 3.06 ms                                                 | 4.83 ms: 1.58x slower                                 |
| sqlglot_normalize        | 146 ms                                                  | 231 ms: 1.58x slower                                  |
| xml_etree_process        | 86.5 ms                                                 | 137 ms: 1.58x slower                                  |
| richards                 | 65.8 ms                                                 | 106 ms: 1.61x slower                                  |
| typing_runtime_protocols | 216 us                                                  | 350 us: 1.62x slower                                  |
| spectral_norm            | 159 ms                                                  | 258 ms: 1.62x slower                                  |
| sqlglot_optimize         | 76.2 ms                                                 | 124 ms: 1.63x slower                                  |
| regex_compile            | 177 ms                                                  | 290 ms: 1.64x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.6 sec: 1.69x slower                                |
| logging_simple           | 8.98 us                                                 | 15.2 us: 1.69x slower                                 |
| pyflate                  | 661 ms                                                  | 1.13 sec: 1.70x slower                                |
| genshi_xml               | 68.3 ms                                                 | 117 ms: 1.71x slower                                  |
| richards_super           | 76.3 ms                                                 | 131 ms: 1.71x slower                                  |
| sympy_integrate          | 29.7 ms                                                 | 51.8 ms: 1.75x slower                                 |
| genshi_text              | 31.7 ms                                                 | 55.9 ms: 1.76x slower                                 |
| pprint_pformat           | 2.00 sec                                                | 3.54 sec: 1.77x slower                                |
| pprint_safe_repr         | 959 ms                                                  | 1.71 sec: 1.78x slower                                |
| float                    | 115 ms                                                  | 206 ms: 1.79x slower                                  |
| django_template          | 46.9 ms                                                 | 85.9 ms: 1.83x slower                                 |
| logging_format           | 9.48 us                                                 | 17.5 us: 1.85x slower                                 |
| sqlglot_transpile        | 2.30 ms                                                 | 4.33 ms: 1.88x slower                                 |
| pickle_pure_python       | 417 us                                                  | 803 us: 1.93x slower                                  |
| sympy_str                | 367 ms                                                  | 709 ms: 1.93x slower                                  |
| comprehensions           | 20.9 us                                                 | 40.4 us: 1.93x slower                                 |
| scimark_monte_carlo      | 89.9 ms                                                 | 174 ms: 1.94x slower                                  |
| scimark_lu               | 154 ms                                                  | 305 ms: 1.98x slower                                  |
| mako                     | 16.1 ms                                                 | 32.0 ms: 1.99x slower                                 |
| hexiom                   | 8.35 ms                                                 | 16.8 ms: 2.01x slower                                 |
| logging_silent           | 130 ns                                                  | 262 ns: 2.02x slower                                  |
| sympy_expand             | 631 ms                                                  | 1.30 sec: 2.07x slower                                |
| chaos                    | 84.7 ms                                                 | 177 ms: 2.09x slower                                  |
| unpickle_pure_python     | 296 us                                                  | 619 us: 2.09x slower                                  |
| sqlglot_parse            | 1.80 ms                                                 | 3.84 ms: 2.13x slower                                 |
| scimark_sor              | 172 ms                                                  | 368 ms: 2.13x slower                                  |
| sympy_sum                | 213 ms                                                  | 479 ms: 2.25x slower                                  |
| raytrace                 | 350 ms                                                  | 804 ms: 2.30x slower                                  |
| nbody                    | 124 ms                                                  | 293 ms: 2.36x slower                                  |
| go                       | 195 ms                                                  | 465 ms: 2.38x slower                                  |
| unpack_sequence          | 73.9 ns                                                 | 180 ns: 2.44x slower                                  |
| deltablue                | 4.56 ms                                                 | 12.0 ms: 2.63x slower                                 |
| Geometric mean           | (ref)                                                   | 1.44x slower                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, pickle_dict, pidigits, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, regex_dna, asyncio_websockets, unpickle
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.15x