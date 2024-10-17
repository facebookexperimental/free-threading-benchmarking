# Results vs. base

- fork: colesbury
- ref: gh_125608_dict_watch
- machine: linux-x86_64
- commit hash: 28871ed
- commit date: 2024-10-16
- overall geometric mean: 1.00x slower
- HPT reliability: 73.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| docutils       | 2.57 sec                                                               | 2.58 sec: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines     | 22.4 ms                                                                | 22.2 ms: 1.01x faster                                                     |
| asyncio_tcp    | 500 ms                                                                 | 506 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (3): asyncio_websockets, async_generators, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 79.5 ms                                                                | 78.5 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 176 ms                                                                 | 169 ms: 1.04x faster                                                      |
| regex_compile  | 130 ms                                                                 | 129 ms: 1.01x faster                                                      |
| regex_v8       | 23.0 ms                                                                | 23.5 ms: 1.02x slower                                                     |
| regex_effbot   | 2.95 ms                                                                | 3.09 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle               | 11.5 us                                                                | 11.2 us: 1.03x faster                                                     |
| unpickle_list        | 4.71 us                                                                | 4.65 us: 1.01x faster                                                     |
| tomli_loads          | 2.10 sec                                                               | 2.08 sec: 1.01x faster                                                    |
| pickle_pure_python   | 308 us                                                                 | 307 us: 1.00x faster                                                      |
| xml_etree_iterparse  | 95.7 ms                                                                | 96.8 ms: 1.01x slower                                                     |
| unpickle_pure_python | 214 us                                                                 | 216 us: 1.01x slower                                                      |
| pickle_list          | 4.85 us                                                                | 4.99 us: 1.03x slower                                                     |
| pickle_dict          | 30.9 us                                                                | 33.0 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (6): json_loads, xml_etree_process, xml_etree_generate, xml_etree_parse, unpickle, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.7 ms                                                                | 22.3 ms: 1.02x faster                                                     |
| django_template | 35.9 ms                                                                | 35.4 ms: 1.01x faster                                                     |
| genshi_xml      | 50.2 ms                                                                | 49.7 ms: 1.01x faster                                                     |
| mako            | 11.6 ms                                                                | 11.8 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pycparser                | 1.20 sec                                                               | 1.14 sec: 1.06x faster                                                    |
| regex_dna                | 176 ms                                                                 | 169 ms: 1.04x faster                                                      |
| pickle                   | 11.5 us                                                                | 11.2 us: 1.03x faster                                                     |
| logging_silent           | 103 ns                                                                 | 100 ns: 1.03x faster                                                      |
| pyflate                  | 454 ms                                                                 | 445 ms: 1.02x faster                                                      |
| scimark_fft              | 342 ms                                                                 | 336 ms: 1.02x faster                                                      |
| genshi_text              | 22.7 ms                                                                | 22.3 ms: 1.02x faster                                                     |
| raytrace                 | 264 ms                                                                 | 260 ms: 1.02x faster                                                      |
| meteor_contest           | 103 ms                                                                 | 102 ms: 1.01x faster                                                      |
| unpickle_list            | 4.71 us                                                                | 4.65 us: 1.01x faster                                                     |
| float                    | 79.5 ms                                                                | 78.5 ms: 1.01x faster                                                     |
| django_template          | 35.9 ms                                                                | 35.4 ms: 1.01x faster                                                     |
| fannkuch                 | 382 ms                                                                 | 377 ms: 1.01x faster                                                      |
| tomli_loads              | 2.10 sec                                                               | 2.08 sec: 1.01x faster                                                    |
| json                     | 4.92 ms                                                                | 4.87 ms: 1.01x faster                                                     |
| logging_format           | 6.80 us                                                                | 6.73 us: 1.01x faster                                                     |
| typing_runtime_protocols | 158 us                                                                 | 157 us: 1.01x faster                                                      |
| genshi_xml               | 50.2 ms                                                                | 49.7 ms: 1.01x faster                                                     |
| bpe_tokeniser            | 4.36 sec                                                               | 4.32 sec: 1.01x faster                                                    |
| deepcopy_reduce          | 2.68 us                                                                | 2.66 us: 1.01x faster                                                     |
| regex_compile            | 130 ms                                                                 | 129 ms: 1.01x faster                                                      |
| richards                 | 46.1 ms                                                                | 45.7 ms: 1.01x faster                                                     |
| chaos                    | 59.3 ms                                                                | 58.8 ms: 1.01x faster                                                     |
| coroutines               | 22.4 ms                                                                | 22.2 ms: 1.01x faster                                                     |
| pprint_pformat           | 1.47 sec                                                               | 1.47 sec: 1.00x faster                                                    |
| pickle_pure_python       | 308 us                                                                 | 307 us: 1.00x faster                                                      |
| unpack_sequence          | 53.1 ns                                                                | 53.0 ns: 1.00x faster                                                     |
| richards_super           | 51.7 ms                                                                | 51.8 ms: 1.00x slower                                                     |
| sympy_integrate          | 19.9 ms                                                                | 20.0 ms: 1.00x slower                                                     |
| go                       | 120 ms                                                                 | 121 ms: 1.00x slower                                                      |
| sqlglot_normalize        | 106 ms                                                                 | 106 ms: 1.00x slower                                                      |
| docutils                 | 2.57 sec                                                               | 2.58 sec: 1.00x slower                                                    |
| sqlglot_optimize         | 53.5 ms                                                                | 53.8 ms: 1.00x slower                                                     |
| pprint_safe_repr         | 710 ms                                                                 | 714 ms: 1.01x slower                                                      |
| bench_thread_pool        | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                     |
| dulwich_log              | 74.1 ms                                                                | 74.6 ms: 1.01x slower                                                     |
| deepcopy_memo            | 30.2 us                                                                | 30.5 us: 1.01x slower                                                     |
| spectral_norm            | 108 ms                                                                 | 108 ms: 1.01x slower                                                      |
| deltablue                | 3.19 ms                                                                | 3.22 ms: 1.01x slower                                                     |
| scimark_sor              | 133 ms                                                                 | 135 ms: 1.01x slower                                                      |
| pathlib                  | 18.5 ms                                                                | 18.7 ms: 1.01x slower                                                     |
| xml_etree_iterparse      | 95.7 ms                                                                | 96.8 ms: 1.01x slower                                                     |
| unpickle_pure_python     | 214 us                                                                 | 216 us: 1.01x slower                                                      |
| asyncio_tcp              | 500 ms                                                                 | 506 ms: 1.01x slower                                                      |
| scimark_lu               | 110 ms                                                                 | 112 ms: 1.01x slower                                                      |
| comprehensions           | 16.9 us                                                                | 17.1 us: 1.01x slower                                                     |
| mako                     | 11.6 ms                                                                | 11.8 ms: 1.02x slower                                                     |
| coverage                 | 81.0 ms                                                                | 82.6 ms: 1.02x slower                                                     |
| regex_v8                 | 23.0 ms                                                                | 23.5 ms: 1.02x slower                                                     |
| crypto_pyaes             | 66.6 ms                                                                | 68.4 ms: 1.03x slower                                                     |
| pickle_list              | 4.85 us                                                                | 4.99 us: 1.03x slower                                                     |
| scimark_sparse_mat_mult  | 4.33 ms                                                                | 4.49 ms: 1.04x slower                                                     |
| regex_effbot             | 2.95 ms                                                                | 3.09 ms: 1.05x slower                                                     |
| mdp                      | 2.35 sec                                                               | 2.48 sec: 1.05x slower                                                    |
| pickle_dict              | 30.9 us                                                                | 33.0 us: 1.07x slower                                                     |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (34): json_loads, create_gc_cycles, nbody, sqlglot_parse, sympy_expand, sqlite_synth, generators, xml_etree_process, xml_etree_generate, sympy_sum, pidigits, nqueens, hexiom, telco, python_startup_no_site, python_startup, thrift, asyncio_websockets, bench_mp_pool, xml_etree_parse, gc_traversal, pylint, sqlglot_transpile, unpickle, 2to3, async_generators, asyncio_tcp_ssl, deepcopy, html5lib, logging_simple, json_dumps, sympy_str, scimark_monte_carlo, tornado_http

# HPT report

- Reliability score: 73.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x