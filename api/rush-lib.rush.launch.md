[Home](./index) &gt; [@microsoft/rush-lib](./rush-lib.md) &gt; [Rush](./rush-lib.rush.md) &gt; [launch](./rush-lib.rush.launch.md)

# Rush.launch method

This API is used by the `@microsoft/rush` front end to launch the "rush" command-line. Third-party tools should not use this API. Instead, they should execute the "rush" binary and start a new NodeJS process.

**Signature:**
```javascript
static launch(launcherVersion: string, isManaged: boolean): void;
```
**Returns:** `void`

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  `launcherVersion` | `string` | The version of the `@microsoft/rush` wrapper used to call invoke the CLI. |
|  `isManaged` | `boolean` | True if the tool was invoked from within a project with a rush.json file, otherwise false. We consider a project without a rush.json to be "unmanaged" and we'll print that to the command line when the tool is executed. This is mainly used for debugging purposes. |
