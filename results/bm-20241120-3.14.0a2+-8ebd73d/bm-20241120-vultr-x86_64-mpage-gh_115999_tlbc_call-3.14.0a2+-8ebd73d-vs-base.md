# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.00x faster
- HPT reliability: 59.05%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 255 ms: 1.00x faster                                                 |
| docutils       | 2.63 sec                                                               | 2.59 sec: 1.01x faster                                               |
| html5lib       | 66.9 ms                                                                | 64.9 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators | 378 ms                                                                 | 385 ms: 1.02x slower                                                 |
| coroutines       | 22.6 ms                                                                | 23.1 ms: 1.03x slower                                                |
| Geometric mean   | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 186 ms: 1.17x faster                                                 |
| float          | 78.8 ms                                                                | 79.8 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.70 ms: 1.06x faster                                                |
| regex_v8       | 23.6 ms                                                                | 22.7 ms: 1.04x faster                                                |
| regex_compile  | 135 ms                                                                 | 130 ms: 1.03x faster                                                 |
| regex_dna      | 177 ms                                                                 | 177 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list        | 5.29 us                                                                | 5.02 us: 1.05x faster                                                |
| pickle_dict        | 32.3 us                                                                | 31.0 us: 1.04x faster                                                |
| unpickle_list      | 4.81 us                                                                | 4.68 us: 1.03x faster                                                |
| pickle_pure_python | 320 us                                                                 | 314 us: 1.02x faster                                                 |
| xml_etree_generate | 86.2 ms                                                                | 84.8 ms: 1.02x faster                                                |
| xml_etree_process  | 60.2 ms                                                                | 59.4 ms: 1.01x faster                                                |
| tomli_loads        | 2.15 sec                                                               | 2.13 sec: 1.01x faster                                               |
| json_dumps         | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                |
| pickle             | 12.3 us                                                                | 12.4 us: 1.01x slower                                                |
| unpickle           | 13.5 us                                                                | 13.9 us: 1.03x slower                                                |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (4): xml_etree_parse, json_loads, unpickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                |
| python_startup_no_site | 7.41 ms                                                                | 7.42 ms: 1.00x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 12.0 ms                                                                | 11.8 ms: 1.01x faster                                                |
| django_template | 35.7 ms                                                                | 35.3 ms: 1.01x faster                                                |
| genshi_text     | 21.9 ms                                                                | 22.4 ms: 1.02x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                 | 217 ms                                                                 | 186 ms: 1.17x faster                                                 |
| gc_traversal             | 3.63 ms                                                                | 3.39 ms: 1.07x faster                                                |
| regex_effbot             | 2.86 ms                                                                | 2.70 ms: 1.06x faster                                                |
| pickle_list              | 5.29 us                                                                | 5.02 us: 1.05x faster                                                |
| pickle_dict              | 32.3 us                                                                | 31.0 us: 1.04x faster                                                |
| regex_v8                 | 23.6 ms                                                                | 22.7 ms: 1.04x faster                                                |
| regex_compile            | 135 ms                                                                 | 130 ms: 1.03x faster                                                 |
| logging_format           | 6.99 us                                                                | 6.79 us: 1.03x faster                                                |
| html5lib                 | 66.9 ms                                                                | 64.9 ms: 1.03x faster                                                |
| unpickle_list            | 4.81 us                                                                | 4.68 us: 1.03x faster                                                |
| logging_simple           | 6.30 us                                                                | 6.16 us: 1.02x faster                                                |
| pickle_pure_python       | 320 us                                                                 | 314 us: 1.02x faster                                                 |
| xml_etree_generate       | 86.2 ms                                                                | 84.8 ms: 1.02x faster                                                |
| mako                     | 12.0 ms                                                                | 11.8 ms: 1.01x faster                                                |
| sqlite_synth             | 2.24 us                                                                | 2.21 us: 1.01x faster                                                |
| pathlib                  | 18.6 ms                                                                | 18.3 ms: 1.01x faster                                                |
| xml_etree_process        | 60.2 ms                                                                | 59.4 ms: 1.01x faster                                                |
| docutils                 | 2.63 sec                                                               | 2.59 sec: 1.01x faster                                               |
| chaos                    | 59.0 ms                                                                | 58.3 ms: 1.01x faster                                                |
| django_template          | 35.7 ms                                                                | 35.3 ms: 1.01x faster                                                |
| typing_runtime_protocols | 160 us                                                                 | 158 us: 1.01x faster                                                 |
| go                       | 122 ms                                                                 | 121 ms: 1.01x faster                                                 |
| deepcopy                 | 266 us                                                                 | 264 us: 1.01x faster                                                 |
| pylint                   | 272 ms                                                                 | 270 ms: 1.01x faster                                                 |
| thrift                   | 752 us                                                                 | 747 us: 1.01x faster                                                 |
| sympy_str                | 275 ms                                                                 | 273 ms: 1.01x faster                                                 |
| scimark_lu               | 113 ms                                                                 | 112 ms: 1.01x faster                                                 |
| tomli_loads              | 2.15 sec                                                               | 2.13 sec: 1.01x faster                                               |
| sympy_sum                | 153 ms                                                                 | 153 ms: 1.01x faster                                                 |
| nqueens                  | 79.2 ms                                                                | 78.8 ms: 1.01x faster                                                |
| comprehensions           | 17.3 us                                                                | 17.2 us: 1.01x faster                                                |
| sqlglot_normalize        | 108 ms                                                                 | 107 ms: 1.00x faster                                                 |
| unpack_sequence          | 47.0 ns                                                                | 46.8 ns: 1.00x faster                                                |
| sympy_integrate          | 20.0 ms                                                                | 19.9 ms: 1.00x faster                                                |
| 2to3                     | 256 ms                                                                 | 255 ms: 1.00x faster                                                 |
| python_startup           | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                |
| crypto_pyaes             | 67.9 ms                                                                | 68.0 ms: 1.00x slower                                                |
| python_startup_no_site   | 7.41 ms                                                                | 7.42 ms: 1.00x slower                                                |
| regex_dna                | 177 ms                                                                 | 177 ms: 1.00x slower                                                 |
| deepcopy_reduce          | 2.65 us                                                                | 2.67 us: 1.01x slower                                                |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.01x slower                                                |
| pprint_pformat           | 1.48 sec                                                               | 1.49 sec: 1.01x slower                                               |
| json_dumps               | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                |
| scimark_sor              | 136 ms                                                                 | 137 ms: 1.01x slower                                                 |
| hexiom                   | 5.96 ms                                                                | 6.02 ms: 1.01x slower                                                |
| pyflate                  | 448 ms                                                                 | 452 ms: 1.01x slower                                                 |
| telco                    | 7.22 ms                                                                | 7.29 ms: 1.01x slower                                                |
| pprint_safe_repr         | 716 ms                                                                 | 723 ms: 1.01x slower                                                 |
| pickle                   | 12.3 us                                                                | 12.4 us: 1.01x slower                                                |
| json                     | 4.61 ms                                                                | 4.66 ms: 1.01x slower                                                |
| float                    | 78.8 ms                                                                | 79.8 ms: 1.01x slower                                                |
| generators               | 29.2 ms                                                                | 29.6 ms: 1.01x slower                                                |
| fannkuch                 | 371 ms                                                                 | 376 ms: 1.01x slower                                                 |
| bpe_tokeniser            | 4.34 sec                                                               | 4.40 sec: 1.01x slower                                               |
| create_gc_cycles         | 1.34 ms                                                                | 1.36 ms: 1.01x slower                                                |
| deepcopy_memo            | 30.3 us                                                                | 30.8 us: 1.02x slower                                                |
| spectral_norm            | 113 ms                                                                 | 115 ms: 1.02x slower                                                 |
| coverage                 | 80.2 ms                                                                | 81.7 ms: 1.02x slower                                                |
| async_generators         | 378 ms                                                                 | 385 ms: 1.02x slower                                                 |
| genshi_text              | 21.9 ms                                                                | 22.4 ms: 1.02x slower                                                |
| coroutines               | 22.6 ms                                                                | 23.1 ms: 1.03x slower                                                |
| scimark_sparse_mat_mult  | 4.48 ms                                                                | 4.62 ms: 1.03x slower                                                |
| unpickle                 | 13.5 us                                                                | 13.9 us: 1.03x slower                                                |
| deltablue                | 3.25 ms                                                                | 3.45 ms: 1.06x slower                                                |
| mdp                      | 2.36 sec                                                               | 2.51 sec: 1.06x slower                                               |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (23): nbody, asyncio_tcp, sqlglot_parse, xml_etree_parse, raytrace, json_loads, scimark_monte_carlo, bench_thread_pool, bench_mp_pool, dulwich_log, unpickle_pure_python, asyncio_websockets, asyncio_tcp_ssl, sqlglot_optimize, pycparser, richards, richards_super, scimark_fft, sympy_expand, xml_etree_iterparse, meteor_contest, genshi_xml, logging_silent

# HPT report

- Reliability score: 59.05% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x