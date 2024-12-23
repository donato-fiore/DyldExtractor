# DyldExtractor
Extract Binaries from Apple's Dyld Shared Cache to be useful in a disassembler. This tool theoretically supports iOS 13-18.

NOTE: This is untested for kernelcaches

# Installation
To install my fork, run:
```
pip3 install git+https://github.com/donato-fiore/DyldExtractor.git
```

# Usage Examples

```

# Listing Framework names containing <Filter Text>
dyldex -l -f <Filter Text> [dyld_shared_cache_path]

# Extracting a framework
dyldex -e SpringBoard.framework/SpringBoard [dyld_shared_cache_path]

# Extracting all frameworks/libraries from a shared cache
dyldex_all [dyld_shared_cache_path]

# Extracting all frameworks/libraries from a shared cache containing name
dyldex_all -f <Filter Text> [dyld_shared_cache_path]

# In any of the above examples, replace "dyldex" and "dyldex_all" with "kextex" and "kextex_all" respectively to extract images from a MH_FILESET kernelcache instead of a DSC

```
