## Keywords

Each line that isn’t a blank line has to start with a Gherkin keyword, followed by any text you like. The only exceptions are the feature and scenario descriptions.

### The primary keywords are:

 - `Feature`
 - `Rule` (as of Gherkin 6)
 - `Example` (or Scenario)
 - `Given`, `When`, `Then`, `And`, `But` for steps (or `*`)
 - `Background`
 - `Scenario Outline` (or `Scenario Template`)
 - `Examples`

### There are a few secondary keywords as well:

 - """ (Doc Strings)
 - | (Data Tables)
 - @ (Tags)
 - \# (Comments)

## Parameters

## Hooks
 - [BeforeTestRun]/[AfterTestRun] (no tag filtering)
 - [BeforeFeature]/[AfterFeature]
 - [BeforeScenario] or [Before]/ [AfterScenario] or [After]
 - [BeforeScenarioBlock]/ [AfterScenarioBlock]
 - [BeforeStep]/ [AfterStep]
