# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 62ea35e
- commit date: 2026-03-15
- overall geometric mean: 1.008x slower
- HPT reliability: 84.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 249 ms: 1.01x faster                                                       |
| docutils       | 2.61 sec                                                               | 2.66 sec: 1.02x slower                                                     |
| sphinx         | 992 ms                                                                 | 1.01 sec: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| coroutines                 | 23.4 ms                                                                | 22.2 ms: 1.05x faster                                                      |
| async_tree_memoization     | 304 ms                                                                 | 290 ms: 1.05x faster                                                       |
| async_tree_none            | 241 ms                                                                 | 233 ms: 1.04x faster                                                       |
| async_tree_none_tg         | 240 ms                                                                 | 233 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 487 ms: 1.03x faster                                                       |
| async_tree_io_tg           | 564 ms                                                                 | 550 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 499 ms: 1.02x faster                                                       |
| async_generators           | 365 ms                                                                 | 359 ms: 1.02x faster                                                       |
| async_tree_io              | 579 ms                                                                 | 573 ms: 1.01x faster                                                       |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                 | 201 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 124 ms                                                                 | 125 ms: 1.01x slower                                                       |
| regex_effbot   | 2.61 ms                                                                | 2.80 ms: 1.07x slower                                                      |
| regex_dna      | 165 ms                                                                 | 179 ms: 1.09x slower                                                       |
| regex_v8       | 20.9 ms                                                                | 23.4 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_process    | 54.7 ms                                                                | 53.0 ms: 1.03x faster                                                      |
| xml_etree_parse      | 131 ms                                                                 | 130 ms: 1.01x faster                                                       |
| xml_etree_iterparse  | 83.2 ms                                                                | 83.8 ms: 1.01x slower                                                      |
| unpickle_pure_python | 198 us                                                                 | 199 us: 1.01x slower                                                       |
| xml_etree_generate   | 77.5 ms                                                                | 78.9 ms: 1.02x slower                                                      |
| json_loads           | 27.1 us                                                                | 27.7 us: 1.02x slower                                                      |
| tomli_loads          | 1.51 sec                                                               | 1.55 sec: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (2): pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                      |
| python_startup_no_site | 7.51 ms                                                                | 7.53 ms: 1.00x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                                | 10.6 ms: 1.01x slower                                                      |
| genshi_xml     | 51.4 ms                                                                | 52.4 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 160 us                                                                 | 151 us: 1.06x faster                                                       |
| logging_simple             | 5.78 us                                                                | 5.46 us: 1.06x faster                                                      |
| coroutines                 | 23.4 ms                                                                | 22.2 ms: 1.05x faster                                                      |
| sqlglot_v2_normalize       | 106 ms                                                                 | 101 ms: 1.05x faster                                                       |
| async_tree_memoization     | 304 ms                                                                 | 290 ms: 1.05x faster                                                       |
| logging_format             | 6.43 us                                                                | 6.17 us: 1.04x faster                                                      |
| scimark_sor                | 85.5 ms                                                                | 82.3 ms: 1.04x faster                                                      |
| async_tree_none            | 241 ms                                                                 | 233 ms: 1.04x faster                                                       |
| xml_etree_process          | 54.7 ms                                                                | 53.0 ms: 1.03x faster                                                      |
| pathlib                    | 17.9 ms                                                                | 17.3 ms: 1.03x faster                                                      |
| async_tree_none_tg         | 240 ms                                                                 | 233 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 487 ms: 1.03x faster                                                       |
| chaos                      | 53.1 ms                                                                | 51.8 ms: 1.02x faster                                                      |
| async_tree_io_tg           | 564 ms                                                                 | 550 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 499 ms: 1.02x faster                                                       |
| meteor_contest             | 98.6 ms                                                                | 96.7 ms: 1.02x faster                                                      |
| deltablue                  | 2.71 ms                                                                | 2.67 ms: 1.02x faster                                                      |
| async_generators           | 365 ms                                                                 | 359 ms: 1.02x faster                                                       |
| sqlglot_v2_optimize        | 52.0 ms                                                                | 51.4 ms: 1.01x faster                                                      |
| async_tree_io              | 579 ms                                                                 | 573 ms: 1.01x faster                                                       |
| logging_silent             | 81.8 ns                                                                | 81.0 ns: 1.01x faster                                                      |
| mdp                        | 1.21 sec                                                               | 1.20 sec: 1.01x faster                                                     |
| fannkuch                   | 343 ms                                                                 | 341 ms: 1.01x faster                                                       |
| 2to3                       | 251 ms                                                                 | 249 ms: 1.01x faster                                                       |
| xml_etree_parse            | 131 ms                                                                 | 130 ms: 1.01x faster                                                       |
| scimark_monte_carlo        | 51.8 ms                                                                | 51.5 ms: 1.00x faster                                                      |
| python_startup             | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                      |
| python_startup_no_site     | 7.51 ms                                                                | 7.53 ms: 1.00x slower                                                      |
| comprehensions             | 14.9 us                                                                | 14.9 us: 1.00x slower                                                      |
| xml_etree_iterparse        | 83.2 ms                                                                | 83.8 ms: 1.01x slower                                                      |
| regex_compile              | 124 ms                                                                 | 125 ms: 1.01x slower                                                       |
| unpickle_pure_python       | 198 us                                                                 | 199 us: 1.01x slower                                                       |
| create_gc_cycles           | 1.85 ms                                                                | 1.87 ms: 1.01x slower                                                      |
| bench_thread_pool          | 1.31 ms                                                                | 1.33 ms: 1.01x slower                                                      |
| spectral_norm              | 76.8 ms                                                                | 77.8 ms: 1.01x slower                                                      |
| deepcopy_memo              | 22.3 us                                                                | 22.6 us: 1.01x slower                                                      |
| pidigits                   | 198 ms                                                                 | 201 ms: 1.01x slower                                                       |
| mako                       | 10.4 ms                                                                | 10.6 ms: 1.01x slower                                                      |
| dulwich_log                | 69.6 ms                                                                | 70.6 ms: 1.02x slower                                                      |
| thrift                     | 791 us                                                                 | 804 us: 1.02x slower                                                       |
| xml_etree_generate         | 77.5 ms                                                                | 78.9 ms: 1.02x slower                                                      |
| scimark_lu                 | 78.6 ms                                                                | 80.1 ms: 1.02x slower                                                      |
| pyflate                    | 357 ms                                                                 | 363 ms: 1.02x slower                                                       |
| deepcopy                   | 225 us                                                                 | 229 us: 1.02x slower                                                       |
| genshi_xml                 | 51.4 ms                                                                | 52.4 ms: 1.02x slower                                                      |
| sphinx                     | 992 ms                                                                 | 1.01 sec: 1.02x slower                                                     |
| docutils                   | 2.61 sec                                                               | 2.66 sec: 1.02x slower                                                     |
| sqlite_synth               | 2.17 us                                                                | 2.21 us: 1.02x slower                                                      |
| many_optionals             | 965 us                                                                 | 985 us: 1.02x slower                                                       |
| coverage                   | 81.3 ms                                                                | 83.1 ms: 1.02x slower                                                      |
| hexiom                     | 5.69 ms                                                                | 5.82 ms: 1.02x slower                                                      |
| json_loads                 | 27.1 us                                                                | 27.7 us: 1.02x slower                                                      |
| tomli_loads                | 1.51 sec                                                               | 1.55 sec: 1.02x slower                                                     |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.20 ms: 1.03x slower                                                      |
| sqlglot_v2_transpile       | 1.48 ms                                                                | 1.52 ms: 1.03x slower                                                      |
| richards_super             | 21.3 ms                                                                | 22.1 ms: 1.04x slower                                                      |
| scimark_sparse_mat_mult    | 4.15 ms                                                                | 4.30 ms: 1.04x slower                                                      |
| pycparser                  | 1.11 sec                                                               | 1.16 sec: 1.04x slower                                                     |
| gc_traversal               | 4.45 ms                                                                | 4.64 ms: 1.04x slower                                                      |
| sympy_integrate            | 19.5 ms                                                                | 20.4 ms: 1.04x slower                                                      |
| pylint                     | 291 ms                                                                 | 305 ms: 1.05x slower                                                       |
| sympy_str                  | 286 ms                                                                 | 300 ms: 1.05x slower                                                       |
| deepcopy_reduce            | 2.38 us                                                                | 2.51 us: 1.05x slower                                                      |
| richards                   | 17.4 ms                                                                | 18.4 ms: 1.06x slower                                                      |
| sympy_sum                  | 161 ms                                                                 | 171 ms: 1.06x slower                                                       |
| raytrace                   | 275 ms                                                                 | 293 ms: 1.07x slower                                                       |
| regex_effbot               | 2.61 ms                                                                | 2.80 ms: 1.07x slower                                                      |
| regex_dna                  | 165 ms                                                                 | 179 ms: 1.09x slower                                                       |
| regex_v8                   | 20.9 ms                                                                | 23.4 ms: 1.12x slower                                                      |
| generators                 | 28.2 ms                                                                | 35.0 ms: 1.24x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (24): bench_mp_pool, django_template, async_tree_memoization_tg, float, go, pickle_pure_python, html5lib, nqueens, shortest_path, nbody, connected_components, bpe_tokeniser, k_core, asyncio_websockets, genshi_text, crypto_pyaes, json_dumps, scimark_fft, telco, sympy_expand, json, pprint_pformat, subparsers, pprint_safe_repr
Ignored benchmarks (8) of results/bm-20260314-3.15.0a7+-788c329-JIT/bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7+-788c329.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 84.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x