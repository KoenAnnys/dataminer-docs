---
uid: General_Main_Release_10.3.0_CU12
---

# General Main Release 10.3.0 CU12 – Preview

> [!IMPORTANT]
> We are still working on this release. Some release notes may still be modified or moved to a later release. Check back soon for updates!

> [!TIP]
> For information on how to upgrade DataMiner, see [Upgrading a DataMiner Agent](xref:Upgrading_a_DataMiner_Agent).

### Enhancements

#### DataMiner upgrade: Enhanced robustness of MSI package installations [ID_38376]

<!-- MR 10.3.0 [CU12] - FR 10.4.2 [CU0] -->

Up to now, during a DataMiner upgrade, in some cases, MSI packages would fail to install and throw one of the following errors:

- `The Installer has insufficient privileges to access this directory: ...`
- `Service ... could not be installed. Verify that you have sufficient privileges to install system services.`

From now on, when one of the above-mentioned errors is thrown, it will no longer be necessary to restart the entire upgrade procedure. Instead, a retry will be attempted during the running upgrade.

### Fixes

#### Correlation: Alarm buckets would not get cleaned up when alarms were cleared before the end of the time frame specified in the 'Collect events for ... after first event, then evaluate conditions and execute actions' setting [ID_38292]

<!-- MR 10.3.0 [CU12]/10.4.0 [CU0] - FR 10.4.3 -->

Up to now, when alarms were cleared before the end of the time frame specified in the *Collect events for ... after first event, then evaluate conditions and execute actions* correlation rule setting, the alarm buckets would not get cleaned up.

From now on, when a correlation rule is configured to use the *Collect events for ... after first event, then evaluate conditions and execute actions* trigger mechanism, all alarm buckets will be properly cleaned up, unless there are actions that need to be executed either when the base alarms are updated or when alarms are cleared.