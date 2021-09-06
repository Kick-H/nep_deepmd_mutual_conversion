# nep_deepmd_mutual_conversion

## Purpose:
    Convert deepmd input file format to train.in of nep.
    The structure of the input directory is as follows:
    deepmd/
    ├── init.000    #Type:1 (has virial)
    │   ├── set.000
    │   │   ├── box.npy
    │   │   ├── coord.npy
    │   │   ├── energy.npy
    │   │   ├── force.npy
    │   │   └── virial.npy
    │   ├── type_map.raw
    │   └── type.raw
    └── init.001     # Type:2 (no virial)
        ├── set.000
        │   ├── box.npy
        │   ├── coord.npy
        │   ├── energy.npy
        │   └── force.npy
        ├── type_map.raw
        └── type.raw
    If you have calculated deepmd, then the above file directory should be easy for you to get.

## deep2nep:
>> python deep2nep.py deepmd

## nep2dep:
>> python nep2xyz.py nep

## Refs:
https://github.com/deepmodeling/dpdata

http://dplibrary.deepmd.net/#/project_details?project_id=202010.002

## Author:
"Ke Xu <twtdq(at)qq.com>"
