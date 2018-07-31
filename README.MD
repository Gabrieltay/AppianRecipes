# APPIAN Receipes

## Switch Case
```Sail
with(
    local!result:fn!choose(
    wherecontains(
      ri!case,
      {
        cons!BGP_CMN_CASE_1,
        cons!BGP_CMN_CASE_2,
        cons!BGP_CMN_CASE_3
      }
    ),
    {
        result: "Case 1 Function ..."
    },
    {
        result: "Case 2 Function ..."
    },
    {
        result: "Case 3 Function ..."
    }
  ),
  local!result
)
```

## List Casting
```Sail
with(
    cast('type!{http://www.appian.com/ae/types/2009}Integer?list',
    {
        3.2, 1.0, 2.2
    }
    )
)
```
##### Output
```
List of Number (Integer): 3 items
    3
    1
    2
```

## Null Check for Fields within nested dictionary
```Sail
load(
  local!aa: {
    {a1: 11},
    {a1: 12}
  },
  local!bb: {
    {a1: null},
    {a1: 22}
  },
  any(
    fn!isnull,
    {
      local!aa.a1,
      local!bb.a1
    }
  )
)
```
##### Output
```
true
```
