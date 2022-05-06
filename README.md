# EXT\_copyrights

## Contributors

* Takahiro Aoyagi, Mozilla, [@takahirox](https://github.com/takahirox)

## Status

Prototype

## Dependencies

Written against the glTF 2.0 spec.

## Overview

T.B.D.

[`glTF core spec`](https://www.khronos.org/registry/glTF/specs/2.0/glTF-2.0.html) has a copyright field. But the field takes any strings. It is hard for applications to determine from the field to prohibit certain uses depending on the copyright or licence. This extension provides more structured copyrights information in glTF.

## Example

```
{
    "asset": {
        "extensions": {
            "EXT_copyrights": {
                "authors": [
                    "John Smith",
                    "Ichiro Tanaka"
                ],
                "version": "1.0.0",
                "uri": "https://www.dummy.com/dummy.html",
                "license": "CC BY-SA 3.0 US",
                "licenseUri": "https://creativecommons.org/licenses/by-sa/3.0/us/",
                "unpermitted": [
                    "redistribution",
                    "commersial use",
                    "modification"
                ]
            }
        }
    }
}
```

## Fallback

T.B.D.

## Copyright types

| Property | Type | Description | Requires |
|:------|:------|:------|:------|
| `authors` | `string[1-*]` | | Yes |
| `version` | `string` | | Yes |
| `uri` | `string` | | No |
| `copyright` | `string` | | No |
| `license` | `string` | | No |
| `licenseUri` | `string` | | No |
| `extras` | `any` | | No |
| `unpermitted` | `string[1-*]` | T.B.D. any of "redistribution", "commersial use", "modification", ... | No (Should these be specified in the license?) |
