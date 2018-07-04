# APPIAN Receipes

```sail;
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