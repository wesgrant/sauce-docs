---
id: espresso
title: "Configuration Syntax: Espresso"
sidebar_label: Espresso
---


Please refer to the [Common Configuration Syntax Reference](/testrunner-toolkit/configuration/common-syntax)for information regarding fields such as `apiVersion`, `kind`, `suites`, `sauce`, etc.

## Example Configuration

```yaml reference
https://github.com/saucelabs/saucectl-espresso-example/blob/master/.sauce/config.yml
```

## `espresso`

__Description__: Details specific to the `espresso` configuration.

__Type__: *object*

__Example__:
```yaml
espresso:
  app: ./apps/calc.apk
  testApp: ./apps/calc-success.apk
```

### `app`

__Description__: Path to the application. It supports expanded enviornment variable.

__Type__: *string*

__Examples__:
```yaml
  app: ./apps/calc.apk
```

```yaml
  app: $APP
```

### `testApp`

__Description__: Path to the testing application. It supports expanded enviornment variable.

__Type__: *string*

__Examples__:
```yaml
  testApp: ./apps/calc-success.apk
```

```yaml
  testApp: $TEST_APP
```

## `devices`

__Description__: Field for defining device details such as the device name, orientation, and
formVersions.

__Type__: *object*

__Example__:
```yaml
devices:
  - name: "Android GoogleApi Emulator"
    orientation: portrait
    platformVersions:
      - "11.0"
      - "10.0"
```

### `name`

__Description__: Name of the device. All supported devices can be found by following this [link](https://app.saucelabs.com/live/web-testing/virtual)

__Type__: *string*

__Example__:
```yaml
  - name: "Android GoogleApi Emulator"
```

### `orientation`

__Description__: Screen orientation.

__Type__: *enum*

__Values__: *portrait*, *landscape*

__Example__:
```yaml
  orientation: portrait
```

### `platformVersions`

__Description__: Platform version. All supported platform versions can be found by following this [link](https://app.saucelabs.com/live/web-testing/virtual)

__Type__:  *array*

__Example__:

```yaml
  platformVersions:
    - "11.0"
    - "10.0"
```

## `testOptions`

__Description__: A set of parameters allowing you to select tests for the suite based on matching attributes.

__Type__: *object*

__Example__:
```yaml
testOptions:
  class:
    - com.example.android.testing.androidjunitrunnersample.CalculatorAddParameterizedTest
  notClass:
    - com.example.android.testing.androidjunitrunnersample.CalculatorInstrumentationTest  
  size: small
  package: com.example.android.testing.androidjunitrunnersample
  annotation: com.android.buzz.MyAnnotation
```

### `class`

__Description__: Instructs `saucectl` to only run the specified classes for this test suite.

__Type__: *array*

__Example__:
```yaml
  class:
    - com.example.android.testing.androidjunitrunnersample.CalculatorAddParameterizedTest
```

### `notClass`

__Description__: Instructs `saucectl` to run all classes for the suite *except* those specified here.

__Type__: *array*

__Example__:
```yaml
  notClass:
    - com.example.android.testing.androidjunitrunnersample.CalculatorInstrumentationTest
```

### `size`

__Description__: Instructs `saucectl` to run only tests that are annotated with the matching size value.

__Type__: *enum*

__Values__: *small*, *medium*, *large*

__Example__:
```yaml
  size: small
```

### `package`

__Description__: Instructs `saucectl` to run only tests in the specified package.

__Type__: *string*

__Example__:
```yaml
  package: com.example.android.testing.androidjunitrunnersample
```

### `annotation`

__Description__: Instructs `saucectl` to run only tests that match a custom annotation that you have set.

__Type__: *string*

__Example__:
```yaml
  annotation: com.android.buzz.MyAnnotation
```
