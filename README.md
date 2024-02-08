# handy-ts
* ## Omit++
  ```ts
  export type OmitStrict<
    T extends Record<string, any>,
    K extends keyof T,
  > = Omit<T, K>;

  export type OmitReplace<
    T extends Record<string, any>,
    U extends Record<string, any>,
  > = keyof U extends (infer R extends keyof T)
    ? Omit<T, R> & U
    : never;

  export type AddOrReplace<
    T extends Record<string, any>,
    U extends Record<string, any>
  > = Omit<T, keyof U> & U;
  ```
