# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 662 ms: 1.50x slower                                  |
| docutils       | 4.01 sec                                                | 4.97 sec: 1.24x slower                                |
| html5lib       | 98.1 ms                                                 | 137 ms: 1.40x slower                                  |
| tornado_http   | 248 ms                                                  | 339 ms: 1.37x slower                                  |
| Geometric mean | (ref)                                                   | 1.37x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| async_tree_io           | 1.38 sec                                                | 1.27 sec: 1.08x faster                                |
| async_tree_cpu_io_mixed | 899 ms                                                  | 959 ms: 1.07x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.08 sec: 1.09x slower                                |
| async_generators        | 592 ms                                                  | 721 ms: 1.22x slower                                  |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.42 sec: 1.22x slower                                |
| coroutines              | 29.2 ms                                                 | 41.7 ms: 1.43x slower                                 |
| Geometric mean          | (ref)                                                   | 1.05x slower                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                  | 211 ms: 1.83x slower                                  |
| nbody          | 124 ms                                                  | 278 ms: 2.25x slower                                  |
| Geometric mean | (ref)                                                   | 1.59x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 37.6 ms: 1.16x slower                                 |
| regex_compile  | 177 ms                                                  | 307 ms: 1.73x slower                                  |
| Geometric mean | (ref)                                                   | 1.18x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 208 ms: 1.13x faster                                  |
| pickle               | 15.4 us                                                 | 14.4 us: 1.07x faster                                 |
| unpickle_list        | 6.67 us                                                 | 7.97 us: 1.20x slower                                 |
| json_loads           | 36.1 us                                                 | 45.6 us: 1.26x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 164 ms: 1.27x slower                                  |
| json_dumps           | 14.9 ms                                                 | 19.0 ms: 1.27x slower                                 |
| xml_etree_process    | 86.5 ms                                                 | 127 ms: 1.47x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.32 sec: 1.54x slower                                |
| unpickle_pure_python | 296 us                                                  | 547 us: 1.85x slower                                  |
| pickle_pure_python   | 417 us                                                  | 801 us: 1.92x slower                                  |
| Geometric mean       | (ref)                                                   | 1.22x slower                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle_list, pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 19.3 ms: 1.32x slower                                 |
| python_startup         | 22.0 ms                                                 | 29.1 ms: 1.32x slower                                 |
| Geometric mean         | (ref)                                                   | 1.32x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 53.7 ms: 1.69x slower                                 |
| genshi_xml      | 68.3 ms                                                 | 125 ms: 1.83x slower                                  |
| django_template | 46.9 ms                                                 | 86.4 ms: 1.84x slower                                 |
| mako            | 16.1 ms                                                 | 31.1 ms: 1.94x slower                                 |
| Geometric mean  | (ref)                                                   | 1.82x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool            | 19.4 ms                                                 | 14.4 ms: 1.34x faster                                 |
| gc_traversal             | 5.91 ms                                                 | 4.51 ms: 1.31x faster                                 |
| create_gc_cycles         | 2.46 ms                                                 | 1.93 ms: 1.28x faster                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| xml_etree_parse          | 236 ms                                                  | 208 ms: 1.13x faster                                  |
| async_tree_io            | 1.38 sec                                                | 1.27 sec: 1.08x faster                                |
| pickle                   | 15.4 us                                                 | 14.4 us: 1.07x faster                                 |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 959 ms: 1.07x slower                                  |
| sqlite_synth             | 4.07 us                                                 | 4.39 us: 1.08x slower                                 |
| asyncio_tcp              | 985 ms                                                  | 1.08 sec: 1.09x slower                                |
| deepcopy                 | 484 us                                                  | 556 us: 1.15x slower                                  |
| regex_v8                 | 32.4 ms                                                 | 37.6 ms: 1.16x slower                                 |
| pathlib                  | 29.3 ms                                                 | 34.2 ms: 1.17x slower                                 |
| unpickle_list            | 6.67 us                                                 | 7.97 us: 1.20x slower                                 |
| telco                    | 11.4 ms                                                 | 13.8 ms: 1.21x slower                                 |
| async_generators         | 592 ms                                                  | 721 ms: 1.22x slower                                  |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.42 sec: 1.22x slower                                |
| json                     | 6.55 ms                                                 | 8.11 ms: 1.24x slower                                 |
| docutils                 | 4.01 sec                                                | 4.97 sec: 1.24x slower                                |
| pylint                   | 472 ms                                                  | 592 ms: 1.25x slower                                  |
| meteor_contest           | 157 ms                                                  | 198 ms: 1.26x slower                                  |
| json_loads               | 36.1 us                                                 | 45.6 us: 1.26x slower                                 |
| xml_etree_generate       | 129 ms                                                  | 164 ms: 1.27x slower                                  |
| json_dumps               | 14.9 ms                                                 | 19.0 ms: 1.27x slower                                 |
| scimark_fft              | 477 ms                                                  | 616 ms: 1.29x slower                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 9.09 ms: 1.30x slower                                 |
| mdp                      | 3.80 sec                                                | 4.96 sec: 1.31x slower                                |
| python_startup_no_site   | 14.6 ms                                                 | 19.3 ms: 1.32x slower                                 |
| python_startup           | 22.0 ms                                                 | 29.1 ms: 1.32x slower                                 |
| coverage                 | 110 ms                                                  | 148 ms: 1.34x slower                                  |
| dulwich_log              | 100.0 ms                                                | 134 ms: 1.34x slower                                  |
| generators               | 39.2 ms                                                 | 53.4 ms: 1.36x slower                                 |
| deepcopy_memo            | 51.7 us                                                 | 70.5 us: 1.36x slower                                 |
| tornado_http             | 248 ms                                                  | 339 ms: 1.37x slower                                  |
| bench_thread_pool        | 3.06 ms                                                 | 4.26 ms: 1.39x slower                                 |
| html5lib                 | 98.1 ms                                                 | 137 ms: 1.40x slower                                  |
| coroutines               | 29.2 ms                                                 | 41.7 ms: 1.43x slower                                 |
| pycparser                | 1.57 sec                                                | 2.25 sec: 1.43x slower                                |
| fannkuch                 | 543 ms                                                  | 792 ms: 1.46x slower                                  |
| xml_etree_process        | 86.5 ms                                                 | 127 ms: 1.47x slower                                  |
| sympy_integrate          | 29.7 ms                                                 | 44.1 ms: 1.49x slower                                 |
| nqueens                  | 108 ms                                                  | 161 ms: 1.49x slower                                  |
| 2to3                     | 442 ms                                                  | 662 ms: 1.50x slower                                  |
| deepcopy_reduce          | 4.27 us                                                 | 6.40 us: 1.50x slower                                 |
| crypto_pyaes             | 99.8 ms                                                 | 152 ms: 1.52x slower                                  |
| tomli_loads              | 2.80 sec                                                | 4.32 sec: 1.54x slower                                |
| spectral_norm            | 159 ms                                                  | 246 ms: 1.55x slower                                  |
| sqlglot_normalize        | 146 ms                                                  | 227 ms: 1.55x slower                                  |
| thrift                   | 1.11 ms                                                 | 1.74 ms: 1.57x slower                                 |
| sqlglot_optimize         | 76.2 ms                                                 | 123 ms: 1.61x slower                                  |
| richards                 | 65.8 ms                                                 | 107 ms: 1.62x slower                                  |
| typing_runtime_protocols | 216 us                                                  | 354 us: 1.64x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.2 sec: 1.64x slower                                |
| richards_super           | 76.3 ms                                                 | 127 ms: 1.67x slower                                  |
| pyflate                  | 661 ms                                                  | 1.12 sec: 1.69x slower                                |
| genshi_text              | 31.7 ms                                                 | 53.7 ms: 1.69x slower                                 |
| regex_compile            | 177 ms                                                  | 307 ms: 1.73x slower                                  |
| pprint_pformat           | 2.00 sec                                                | 3.52 sec: 1.76x slower                                |
| pprint_safe_repr         | 959 ms                                                  | 1.75 sec: 1.82x slower                                |
| scimark_monte_carlo      | 89.9 ms                                                 | 164 ms: 1.83x slower                                  |
| genshi_xml               | 68.3 ms                                                 | 125 ms: 1.83x slower                                  |
| float                    | 115 ms                                                  | 211 ms: 1.83x slower                                  |
| django_template          | 46.9 ms                                                 | 86.4 ms: 1.84x slower                                 |
| logging_simple           | 8.98 us                                                 | 16.5 us: 1.84x slower                                 |
| unpickle_pure_python     | 296 us                                                  | 547 us: 1.85x slower                                  |
| sympy_str                | 367 ms                                                  | 679 ms: 1.85x slower                                  |
| logging_format           | 9.48 us                                                 | 17.9 us: 1.89x slower                                 |
| comprehensions           | 20.9 us                                                 | 39.9 us: 1.91x slower                                 |
| pickle_pure_python       | 417 us                                                  | 801 us: 1.92x slower                                  |
| hexiom                   | 8.35 ms                                                 | 16.1 ms: 1.93x slower                                 |
| mako                     | 16.1 ms                                                 | 31.1 ms: 1.94x slower                                 |
| sqlglot_transpile        | 2.30 ms                                                 | 4.52 ms: 1.97x slower                                 |
| sympy_expand             | 631 ms                                                  | 1.26 sec: 2.00x slower                                |
| scimark_lu               | 154 ms                                                  | 315 ms: 2.04x slower                                  |
| logging_silent           | 130 ns                                                  | 266 ns: 2.05x slower                                  |
| scimark_sor              | 172 ms                                                  | 353 ms: 2.05x slower                                  |
| chaos                    | 84.7 ms                                                 | 176 ms: 2.07x slower                                  |
| go                       | 195 ms                                                  | 420 ms: 2.15x slower                                  |
| sqlglot_parse            | 1.80 ms                                                 | 4.03 ms: 2.24x slower                                 |
| nbody                    | 124 ms                                                  | 278 ms: 2.25x slower                                  |
| sympy_sum                | 213 ms                                                  | 483 ms: 2.27x slower                                  |
| raytrace                 | 350 ms                                                  | 803 ms: 2.30x slower                                  |
| deltablue                | 4.56 ms                                                 | 11.8 ms: 2.58x slower                                 |
| unpack_sequence          | 73.9 ns                                                 | 194 ns: 2.62x slower                                  |
| Geometric mean           | (ref)                                                   | 1.41x slower                                          |

Benchmark hidden because not significant (13): xml_etree_iterparse, async_tree_memoization_tg, pidigits, pickle_list, pickle_dict, regex_effbot, async_tree_none_tg, asyncio_websockets, regex_dna, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization, unpickle
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.15x