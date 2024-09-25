# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 664 ms: 1.50x slower                                  |
| docutils       | 4.01 sec                                                | 4.86 sec: 1.21x slower                                |
| html5lib       | 98.1 ms                                                 | 157 ms: 1.60x slower                                  |
| tornado_http   | 248 ms                                                  | 320 ms: 1.29x slower                                  |
| Geometric mean | (ref)                                                   | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| async_tree_io           | 1.38 sec                                                | 1.22 sec: 1.13x faster                                |
| async_tree_none_tg      | 521 ms                                                  | 493 ms: 1.06x faster                                  |
| asyncio_websockets      | 772 ms                                                  | 750 ms: 1.03x faster                                  |
| async_tree_cpu_io_mixed | 899 ms                                                  | 945 ms: 1.05x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.12 sec: 1.14x slower                                |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.27 sec: 1.17x slower                                |
| async_generators        | 592 ms                                                  | 724 ms: 1.22x slower                                  |
| coroutines              | 29.2 ms                                                 | 45.6 ms: 1.56x slower                                 |
| Geometric mean          | (ref)                                                   | 1.04x slower                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                  | 200 ms: 1.74x slower                                  |
| nbody          | 124 ms                                                  | 283 ms: 2.28x slower                                  |
| Geometric mean | (ref)                                                   | 1.57x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 33.7 ms: 1.04x slower                                 |
| regex_dna      | 288 ms                                                  | 301 ms: 1.04x slower                                  |
| regex_compile  | 177 ms                                                  | 292 ms: 1.64x slower                                  |
| Geometric mean | (ref)                                                   | 1.15x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 213 ms: 1.11x faster                                  |
| pickle_dict          | 46.5 us                                                 | 42.9 us: 1.09x faster                                 |
| pickle               | 15.4 us                                                 | 14.3 us: 1.08x faster                                 |
| pickle_list          | 6.82 us                                                 | 6.45 us: 1.06x faster                                 |
| unpickle_list        | 6.67 us                                                 | 7.21 us: 1.08x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 158 ms: 1.22x slower                                  |
| json_loads           | 36.1 us                                                 | 45.2 us: 1.25x slower                                 |
| json_dumps           | 14.9 ms                                                 | 18.9 ms: 1.27x slower                                 |
| xml_etree_process    | 86.5 ms                                                 | 124 ms: 1.43x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.14 sec: 1.48x slower                                |
| pickle_pure_python   | 417 us                                                  | 760 us: 1.83x slower                                  |
| unpickle_pure_python | 296 us                                                  | 540 us: 1.83x slower                                  |
| Geometric mean       | (ref)                                                   | 1.18x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 29.5 ms: 1.34x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 20.9 ms: 1.43x slower                                 |
| Geometric mean         | (ref)                                                   | 1.38x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 55.7 ms: 1.75x slower                                 |
| genshi_xml      | 68.3 ms                                                 | 122 ms: 1.79x slower                                  |
| django_template | 46.9 ms                                                 | 84.5 ms: 1.80x slower                                 |
| mako            | 16.1 ms                                                 | 31.9 ms: 1.98x slower                                 |
| Geometric mean  | (ref)                                                   | 1.83x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool            | 19.4 ms                                                 | 13.3 ms: 1.45x faster                                 |
| create_gc_cycles         | 2.46 ms                                                 | 1.82 ms: 1.35x faster                                 |
| gc_traversal             | 5.91 ms                                                 | 4.60 ms: 1.28x faster                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| async_tree_io            | 1.38 sec                                                | 1.22 sec: 1.13x faster                                |
| xml_etree_parse          | 236 ms                                                  | 213 ms: 1.11x faster                                  |
| pickle_dict              | 46.5 us                                                 | 42.9 us: 1.09x faster                                 |
| pickle                   | 15.4 us                                                 | 14.3 us: 1.08x faster                                 |
| async_tree_none_tg       | 521 ms                                                  | 493 ms: 1.06x faster                                  |
| pickle_list              | 6.82 us                                                 | 6.45 us: 1.06x faster                                 |
| asyncio_websockets       | 772 ms                                                  | 750 ms: 1.03x faster                                  |
| regex_v8                 | 32.4 ms                                                 | 33.7 ms: 1.04x slower                                 |
| regex_dna                | 288 ms                                                  | 301 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 945 ms: 1.05x slower                                  |
| unpickle_list            | 6.67 us                                                 | 7.21 us: 1.08x slower                                 |
| pathlib                  | 29.3 ms                                                 | 32.6 ms: 1.11x slower                                 |
| asyncio_tcp              | 985 ms                                                  | 1.12 sec: 1.14x slower                                |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.27 sec: 1.17x slower                                |
| telco                    | 11.4 ms                                                 | 13.4 ms: 1.17x slower                                 |
| docutils                 | 4.01 sec                                                | 4.86 sec: 1.21x slower                                |
| xml_etree_generate       | 129 ms                                                  | 158 ms: 1.22x slower                                  |
| async_generators         | 592 ms                                                  | 724 ms: 1.22x slower                                  |
| deepcopy                 | 484 us                                                  | 594 us: 1.23x slower                                  |
| pylint                   | 472 ms                                                  | 582 ms: 1.23x slower                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 8.70 ms: 1.25x slower                                 |
| json_loads               | 36.1 us                                                 | 45.2 us: 1.25x slower                                 |
| meteor_contest           | 157 ms                                                  | 199 ms: 1.26x slower                                  |
| json_dumps               | 14.9 ms                                                 | 18.9 ms: 1.27x slower                                 |
| tornado_http             | 248 ms                                                  | 320 ms: 1.29x slower                                  |
| scimark_fft              | 477 ms                                                  | 617 ms: 1.29x slower                                  |
| bench_thread_pool        | 3.06 ms                                                 | 4.01 ms: 1.31x slower                                 |
| json                     | 6.55 ms                                                 | 8.61 ms: 1.31x slower                                 |
| python_startup           | 22.0 ms                                                 | 29.5 ms: 1.34x slower                                 |
| mdp                      | 3.80 sec                                                | 5.10 sec: 1.34x slower                                |
| deepcopy_memo            | 51.7 us                                                 | 69.7 us: 1.35x slower                                 |
| deepcopy_reduce          | 4.27 us                                                 | 5.85 us: 1.37x slower                                 |
| pycparser                | 1.57 sec                                                | 2.16 sec: 1.38x slower                                |
| coverage                 | 110 ms                                                  | 151 ms: 1.38x slower                                  |
| dulwich_log              | 100.0 ms                                                | 140 ms: 1.40x slower                                  |
| generators               | 39.2 ms                                                 | 54.9 ms: 1.40x slower                                 |
| nqueens                  | 108 ms                                                  | 152 ms: 1.41x slower                                  |
| python_startup_no_site   | 14.6 ms                                                 | 20.9 ms: 1.43x slower                                 |
| xml_etree_process        | 86.5 ms                                                 | 124 ms: 1.43x slower                                  |
| fannkuch                 | 543 ms                                                  | 783 ms: 1.44x slower                                  |
| tomli_loads              | 2.80 sec                                                | 4.14 sec: 1.48x slower                                |
| sympy_integrate          | 29.7 ms                                                 | 43.9 ms: 1.48x slower                                 |
| 2to3                     | 442 ms                                                  | 664 ms: 1.50x slower                                  |
| spectral_norm            | 159 ms                                                  | 247 ms: 1.55x slower                                  |
| coroutines               | 29.2 ms                                                 | 45.6 ms: 1.56x slower                                 |
| thrift                   | 1.11 ms                                                 | 1.75 ms: 1.57x slower                                 |
| sqlglot_normalize        | 146 ms                                                  | 230 ms: 1.58x slower                                  |
| crypto_pyaes             | 99.8 ms                                                 | 157 ms: 1.58x slower                                  |
| typing_runtime_protocols | 216 us                                                  | 342 us: 1.58x slower                                  |
| html5lib                 | 98.1 ms                                                 | 157 ms: 1.60x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.1 sec: 1.62x slower                                |
| sqlglot_optimize         | 76.2 ms                                                 | 124 ms: 1.63x slower                                  |
| regex_compile            | 177 ms                                                  | 292 ms: 1.64x slower                                  |
| logging_simple           | 8.98 us                                                 | 15.2 us: 1.70x slower                                 |
| richards                 | 65.8 ms                                                 | 112 ms: 1.70x slower                                  |
| pyflate                  | 661 ms                                                  | 1.13 sec: 1.71x slower                                |
| richards_super           | 76.3 ms                                                 | 133 ms: 1.74x slower                                  |
| float                    | 115 ms                                                  | 200 ms: 1.74x slower                                  |
| logging_format           | 9.48 us                                                 | 16.6 us: 1.75x slower                                 |
| genshi_text              | 31.7 ms                                                 | 55.7 ms: 1.75x slower                                 |
| pprint_pformat           | 2.00 sec                                                | 3.55 sec: 1.78x slower                                |
| pprint_safe_repr         | 959 ms                                                  | 1.71 sec: 1.79x slower                                |
| genshi_xml               | 68.3 ms                                                 | 122 ms: 1.79x slower                                  |
| django_template          | 46.9 ms                                                 | 84.5 ms: 1.80x slower                                 |
| scimark_monte_carlo      | 89.9 ms                                                 | 163 ms: 1.81x slower                                  |
| pickle_pure_python       | 417 us                                                  | 760 us: 1.83x slower                                  |
| unpickle_pure_python     | 296 us                                                  | 540 us: 1.83x slower                                  |
| comprehensions           | 20.9 us                                                 | 38.3 us: 1.83x slower                                 |
| sympy_str                | 367 ms                                                  | 685 ms: 1.87x slower                                  |
| logging_silent           | 130 ns                                                  | 246 ns: 1.89x slower                                  |
| scimark_sor              | 172 ms                                                  | 341 ms: 1.98x slower                                  |
| mako                     | 16.1 ms                                                 | 31.9 ms: 1.98x slower                                 |
| sqlglot_transpile        | 2.30 ms                                                 | 4.58 ms: 1.99x slower                                 |
| hexiom                   | 8.35 ms                                                 | 16.7 ms: 2.01x slower                                 |
| sympy_expand             | 631 ms                                                  | 1.27 sec: 2.01x slower                                |
| scimark_lu               | 154 ms                                                  | 314 ms: 2.04x slower                                  |
| chaos                    | 84.7 ms                                                 | 175 ms: 2.07x slower                                  |
| go                       | 195 ms                                                  | 411 ms: 2.10x slower                                  |
| sqlglot_parse            | 1.80 ms                                                 | 3.99 ms: 2.22x slower                                 |
| sympy_sum                | 213 ms                                                  | 476 ms: 2.23x slower                                  |
| nbody                    | 124 ms                                                  | 283 ms: 2.28x slower                                  |
| raytrace                 | 350 ms                                                  | 807 ms: 2.31x slower                                  |
| deltablue                | 4.56 ms                                                 | 11.4 ms: 2.50x slower                                 |
| unpack_sequence          | 73.9 ns                                                 | 200 ns: 2.71x slower                                  |
| Geometric mean           | (ref)                                                   | 1.40x slower                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, async_tree_memoization_tg, pidigits, async_tree_memoization, unpickle, regex_effbot, async_tree_cpu_io_mixed_tg, async_tree_none, sqlite_synth
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.15x