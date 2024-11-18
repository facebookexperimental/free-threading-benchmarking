# Results vs. base

- fork: colesbury
- ref: cheaper_steal
- machine: linux-x86_64
- commit hash: ed7085a
- commit date: 2024-11-18
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 422 ms                                                                 | 410 ms: 1.03x faster                                               |
| docutils       | 3.41 sec                                                               | 3.34 sec: 1.02x faster                                             |
| html5lib       | 108 ms                                                                 | 102 ms: 1.05x faster                                               |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines       | 32.2 ms                                                                | 29.3 ms: 1.10x faster                                              |
| async_generators | 500 ms                                                                 | 485 ms: 1.03x faster                                               |
| asyncio_tcp_ssl  | 1.84 sec                                                               | 1.80 sec: 1.02x faster                                             |
| Geometric mean   | (ref)                                                                  | 1.03x faster                                                       |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| nbody          | 204 ms                                                                 | 192 ms: 1.06x faster                                               |
| float          | 154 ms                                                                 | 147 ms: 1.04x faster                                               |
| pidigits       | 188 ms                                                                 | 186 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_compile  | 231 ms                                                                 | 226 ms: 1.02x faster                                               |
| regex_effbot   | 2.92 ms                                                                | 2.85 ms: 1.02x faster                                              |
| regex_dna      | 189 ms                                                                 | 191 ms: 1.01x slower                                               |
| regex_v8       | 25.0 ms                                                                | 25.3 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| tomli_loads          | 3.27 sec                                                               | 3.14 sec: 1.04x faster                                             |
| pickle               | 12.7 us                                                                | 12.2 us: 1.04x faster                                              |
| unpickle_pure_python | 432 us                                                                 | 422 us: 1.02x faster                                               |
| json_dumps           | 15.5 ms                                                                | 15.1 ms: 1.02x faster                                              |
| xml_etree_generate   | 114 ms                                                                 | 112 ms: 1.02x faster                                               |
| pickle_pure_python   | 633 us                                                                 | 620 us: 1.02x faster                                               |
| xml_etree_process    | 94.0 ms                                                                | 92.2 ms: 1.02x faster                                              |
| unpickle_list        | 5.16 us                                                                | 5.09 us: 1.01x faster                                              |
| xml_etree_iterparse  | 109 ms                                                                 | 108 ms: 1.01x faster                                               |
| pickle_list          | 5.12 us                                                                | 5.07 us: 1.01x faster                                              |
| pickle_dict          | 32.6 us                                                                | 32.7 us: 1.00x slower                                              |
| xml_etree_parse      | 133 ms                                                                 | 134 ms: 1.01x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                       |

Benchmark hidden because not significant (2): unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 10.4 ms                                                                | 10.3 ms: 1.00x faster                                              |
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                              |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_text     | 41.6 ms                                                                | 38.9 ms: 1.07x faster                                              |
| genshi_xml      | 83.3 ms                                                                | 78.5 ms: 1.06x faster                                              |
| django_template | 66.1 ms                                                                | 63.2 ms: 1.05x faster                                              |
| mako            | 21.3 ms                                                                | 21.4 ms: 1.01x slower                                              |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                       |

All benchmarks:
===============

| Benchmark               | bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1+-4cd1076 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines              | 32.2 ms                                                                | 29.3 ms: 1.10x faster                                              |
| logging_silent          | 224 ns                                                                 | 206 ns: 1.08x faster                                               |
| genshi_text             | 41.6 ms                                                                | 38.9 ms: 1.07x faster                                              |
| generators              | 41.6 ms                                                                | 39.1 ms: 1.06x faster                                              |
| nbody                   | 204 ms                                                                 | 192 ms: 1.06x faster                                               |
| genshi_xml              | 83.3 ms                                                                | 78.5 ms: 1.06x faster                                              |
| scimark_sparse_mat_mult | 6.07 ms                                                                | 5.72 ms: 1.06x faster                                              |
| fannkuch                | 593 ms                                                                 | 560 ms: 1.06x faster                                               |
| scimark_sor             | 278 ms                                                                 | 263 ms: 1.06x faster                                               |
| pyflate                 | 800 ms                                                                 | 761 ms: 1.05x faster                                               |
| richards                | 93.2 ms                                                                | 88.6 ms: 1.05x faster                                              |
| scimark_fft             | 425 ms                                                                 | 404 ms: 1.05x faster                                               |
| deepcopy                | 446 us                                                                 | 425 us: 1.05x faster                                               |
| html5lib                | 108 ms                                                                 | 102 ms: 1.05x faster                                               |
| django_template         | 66.1 ms                                                                | 63.2 ms: 1.05x faster                                              |
| float                   | 154 ms                                                                 | 147 ms: 1.04x faster                                               |
| deepcopy_reduce         | 4.66 us                                                                | 4.47 us: 1.04x faster                                              |
| go                      | 309 ms                                                                 | 296 ms: 1.04x faster                                               |
| tomli_loads             | 3.27 sec                                                               | 3.14 sec: 1.04x faster                                             |
| richards_super          | 111 ms                                                                 | 107 ms: 1.04x faster                                               |
| sqlglot_parse           | 2.92 ms                                                                | 2.80 ms: 1.04x faster                                              |
| hexiom                  | 12.7 ms                                                                | 12.2 ms: 1.04x faster                                              |
| deltablue               | 9.48 ms                                                                | 9.11 ms: 1.04x faster                                              |
| pickle                  | 12.7 us                                                                | 12.2 us: 1.04x faster                                              |
| scimark_monte_carlo     | 130 ms                                                                 | 125 ms: 1.04x faster                                               |
| nqueens                 | 117 ms                                                                 | 113 ms: 1.04x faster                                               |
| scimark_lu              | 252 ms                                                                 | 243 ms: 1.04x faster                                               |
| sqlglot_transpile       | 3.41 ms                                                                | 3.29 ms: 1.04x faster                                              |
| chaos                   | 124 ms                                                                 | 120 ms: 1.04x faster                                               |
| deepcopy_memo           | 55.2 us                                                                | 53.4 us: 1.04x faster                                              |
| meteor_contest          | 142 ms                                                                 | 137 ms: 1.03x faster                                               |
| sqlglot_normalize       | 184 ms                                                                 | 179 ms: 1.03x faster                                               |
| thrift                  | 1.29 ms                                                                | 1.26 ms: 1.03x faster                                              |
| async_generators        | 500 ms                                                                 | 485 ms: 1.03x faster                                               |
| mdp                     | 3.09 sec                                                               | 3.00 sec: 1.03x faster                                             |
| unpack_sequence         | 149 ns                                                                 | 145 ns: 1.03x faster                                               |
| 2to3                    | 422 ms                                                                 | 410 ms: 1.03x faster                                               |
| comprehensions          | 31.1 us                                                                | 30.3 us: 1.03x faster                                              |
| bpe_tokeniser           | 6.25 sec                                                               | 6.10 sec: 1.02x faster                                             |
| asyncio_tcp_ssl         | 1.84 sec                                                               | 1.80 sec: 1.02x faster                                             |
| regex_compile           | 231 ms                                                                 | 226 ms: 1.02x faster                                               |
| unpickle_pure_python    | 432 us                                                                 | 422 us: 1.02x faster                                               |
| regex_effbot            | 2.92 ms                                                                | 2.85 ms: 1.02x faster                                              |
| json_dumps              | 15.5 ms                                                                | 15.1 ms: 1.02x faster                                              |
| xml_etree_generate      | 114 ms                                                                 | 112 ms: 1.02x faster                                               |
| logging_format          | 13.4 us                                                                | 13.2 us: 1.02x faster                                              |
| raytrace                | 637 ms                                                                 | 624 ms: 1.02x faster                                               |
| pprint_pformat          | 2.78 sec                                                               | 2.72 sec: 1.02x faster                                             |
| spectral_norm           | 164 ms                                                                 | 161 ms: 1.02x faster                                               |
| pprint_safe_repr        | 1.35 sec                                                               | 1.32 sec: 1.02x faster                                             |
| pickle_pure_python      | 633 us                                                                 | 620 us: 1.02x faster                                               |
| sqlglot_optimize        | 91.2 ms                                                                | 89.5 ms: 1.02x faster                                              |
| xml_etree_process       | 94.0 ms                                                                | 92.2 ms: 1.02x faster                                              |
| docutils                | 3.41 sec                                                               | 3.34 sec: 1.02x faster                                             |
| json                    | 5.29 ms                                                                | 5.19 ms: 1.02x faster                                              |
| sympy_integrate         | 33.5 ms                                                                | 32.9 ms: 1.02x faster                                              |
| logging_simple          | 12.1 us                                                                | 11.9 us: 1.02x faster                                              |
| pathlib                 | 22.1 ms                                                                | 21.7 ms: 1.02x faster                                              |
| crypto_pyaes            | 109 ms                                                                 | 107 ms: 1.02x faster                                               |
| pycparser               | 1.72 sec                                                               | 1.69 sec: 1.02x faster                                             |
| sympy_str               | 545 ms                                                                 | 537 ms: 1.01x faster                                               |
| sympy_expand            | 1.07 sec                                                               | 1.05 sec: 1.01x faster                                             |
| unpickle_list           | 5.16 us                                                                | 5.09 us: 1.01x faster                                              |
| pidigits                | 188 ms                                                                 | 186 ms: 1.01x faster                                               |
| dulwich_log             | 105 ms                                                                 | 104 ms: 1.01x faster                                               |
| xml_etree_iterparse     | 109 ms                                                                 | 108 ms: 1.01x faster                                               |
| sympy_sum               | 383 ms                                                                 | 379 ms: 1.01x faster                                               |
| pickle_list             | 5.12 us                                                                | 5.07 us: 1.01x faster                                              |
| coverage                | 102 ms                                                                 | 101 ms: 1.01x faster                                               |
| bench_thread_pool       | 3.50 ms                                                                | 3.48 ms: 1.01x faster                                              |
| bench_mp_pool           | 70.1 ms                                                                | 69.7 ms: 1.01x faster                                              |
| telco                   | 9.44 ms                                                                | 9.39 ms: 1.01x faster                                              |
| python_startup_no_site  | 10.4 ms                                                                | 10.3 ms: 1.00x faster                                              |
| python_startup          | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                              |
| pickle_dict             | 32.6 us                                                                | 32.7 us: 1.00x slower                                              |
| create_gc_cycles        | 1.22 ms                                                                | 1.22 ms: 1.01x slower                                              |
| xml_etree_parse         | 133 ms                                                                 | 134 ms: 1.01x slower                                               |
| regex_dna               | 189 ms                                                                 | 191 ms: 1.01x slower                                               |
| mako                    | 21.3 ms                                                                | 21.4 ms: 1.01x slower                                              |
| regex_v8                | 25.0 ms                                                                | 25.3 ms: 1.01x slower                                              |
| gc_traversal            | 2.39 ms                                                                | 2.71 ms: 1.13x slower                                              |
| Geometric mean          | (ref)                                                                  | 1.02x faster                                                       |

Benchmark hidden because not significant (7): pylint, typing_runtime_protocols, unpickle, json_loads, asyncio_tcp, asyncio_websockets, sqlite_synth

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x