# Kenaz

The overall architecture is a monorepo that has all dev dependencies hoisted to the top directory.

At the moment, we would like to make sure that:

- Each component is atomic and can be imported like:

```tsx
import { Button } from "@kenaz/components";
```

- The components should be:

  - self-contained
  - Use the latest react versions
  - Use react-native-web
  - Use @emotion/native OR @emotion/primitive <- we have yet to determine if this primitive is any better, as it's somewhat staled compared to rnw

- We also want our component library to be usable in both web and native using the exact same import statement.
- How can this be done? Can metro bundler look for `.native` file as an alternative?
