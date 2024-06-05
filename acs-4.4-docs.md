6/5/24, 2:28 PM About Telemetry | Telemetry | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.1b1097d5-2de7-41cb-9def-4bc999a40dff.001.png)![](Aspose.Words.1b1097d5-2de7-41cb-9def-4bc999a40dff.002.png)

About Telemetry

- [Information collected by Telemetry](#_page0_x39.00_y384.75)

Red Hat Advanced Cluster Security for Kubernetes (RHACS) collects anonymized aggregated information about product usage and product configuration. It helps

Red Hat understand how everyone uses the product and identify areas to prioritize for improvements. In addition, Red Hat uses this information to improve the user experience.

<a name="_page0_x39.00_y384.75"></a>Information collected by Telemetry

Telemetry does not collect identifying information such as user names, passwords, or the names or addresses of user resources.

Z Telemetry data collection is enabled by default, except for the ![](Aspose.Words.1b1097d5-2de7-41cb-9def-4bc999a40dff.003.png)![](Aspose.Words.1b1097d5-2de7-41cb-9def-4bc999a40dff.004.png)installations with the offline mode enabled.

Telemetry collects the following information:

- API,  roxctl CLI, and user interface (UI) features and settings to know how you use Red Hat Advanced Cluster Security for Kubernetes (RHACS), which helps prioritize efforts.
- The time you spend on UI screens to help us improve user experience.
- The integrations are used to know if there are integrations that you have never used.
- The number of connected secured clusters and their configurations.
- Errors you encounter to identify the most common problems.
https://docs.openshift.com/acs/4.4/telemetry/about-telemetry.html 2/2

6/5/24, 2:28 PM Viewing the dashboard | Operating | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.001.png)![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.002.png)

Viewing the dashboard

- [Status bar](#_page1_x39.00_y56.25)
- [Dashboard filter](#_page1_x39.00_y519.75)
- [Widget options](#_page2_x39.00_y56.25)
- [Actionable widgets](#_page2_x39.00_y414.00)
  - [Policy violations by severity](#_page2_x39.00_y485.25)
  - [Images at most risk](#_page3_x39.00_y56.25)
  - [Deployments at most risk](#_page3_x39.00_y305.25)
  - [Aging images](#_page3_x39.00_y462.75)
  - [Policy violations by category](#_page4_x39.00_y56.25)
  - [Compliance by standard](#_page4_x39.00_y423.00)

The Red Hat Advanced Cluster Security for Kubernetes (RHACS) Dashboard provides quick access to the data you need. It contains additional navigation shortcuts and actionable widgets that are easy to filter and customize so that you can focus on the data that matters most to you. You can view information about levels of risk in your environment, compliance status, policy violations, and common vulnerabilities and exposures (CVEs) in images.

When you open the RHACS portal for the first time, the Dashboard![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.003.png)![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.004.png)

- might be empty. After you deploy Sensor in at least one cluster, the Dashboard reflects the status of your environment.

The following sections describe the Dashboard components.

<a name="_page1_x39.00_y56.25"></a>Status bar

The Status Bar provides at-a-glance numerical counters for key resources. The counters reflect what is visible with your current access scope that is defined by the roles associated with your user profile. These counters are clickable, providing fast access to desired list view pages as follows:

Counter Destination![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.005.png)![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.006.png)

Clusters Platform Configuration → Clusters

Nodes Configuration Management → Application &

Infrastructure → Nodes

Violations Violations main menu

Deployments Configuration Management → Application &

Infrastructure → Deployments

Images Vulnerability Management → Dashboard → Images Secrets Configuration Management → Application &

Infrastructure → Secrets

<a name="_page1_x39.00_y519.75"></a>Dashboard filter

The Dashboard includes a top-level filter that applies simultaneously to all widgets. You can select one or more clusters, and one or more namespaces within selected clusters. When no clusters or namespaces are selected, the view automatically switches to All. Any change to the filter is immediately reflected by all widgets, limiting the data they present to the selected scope. The Dashboard filter does not affect the

Status Bar .

<a name="_page2_x39.00_y56.25"></a>Widget options

Some widgets are customizable to help you focus on specific data. Widgets offer different controls that you can use to change how the data is sorted, filter the data, and customize the output of the widget.

Widgets offer two ways to customize different aspects:

- An Options menu, when present, provides specific options applicable to that widget.
- A dynamic axis legend , when present, provides a method to filter data by hiding one or more of the axis categories. For example, in the Policy violations by category widget, you can click on a severity to include or exclude violations of a selected severity from the data.
- Individual widget customization settings are short-lived and are reset ![ref1]![ref2]to the system default upon leaving the Dashboard.

<a name="_page2_x39.00_y414.00"></a>Actionable widgets

The following sections describe the actionable widgets available in the Dashboard.

<a name="_page2_x39.00_y485.25"></a>Policy violations by severity

This widget shows the distribution of violations across severity levels for the Dashboard-filtered scope. Clicking a severity level in the chart takes you to the

Violations page, filtered for that severity and scope. It also lists the three most recent violations of a Critical level policy within the scope you defined in the Dashboard filter. Clicking a specific violation takes you directly to the Violations detail page for that violation.

<a name="_page3_x39.00_y56.25"></a>Images at most risk

This widget lists the top six vulnerable images within the Dashboard-filtered scope, sorted by their computed risk priority, along with the number of critical and important CVEs they contain. Click on an image name to go directly to the Image Findings page under Vulnerability Management . Use the Options menu to focus on fixable CVEs, or further focus on active images.

When clusters or namespaces have been selected in the Dashboard![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.009.png)![](Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.010.png)

- filter, the data displayed is already filtered to active images, or images that are used by deployments within the filtered scope.

<a name="_page3_x39.00_y305.25"></a>Deployments at most risk

This widget provides information about the top deployments at risk in your environment. It displays additional information such as the resource location (cluster and namespace) and the risk priority score. Additionally, you can click on a deployment to view risk information about the deployment; for example, its policy violations and vulnerabilities.

<a name="_page3_x39.00_y462.75"></a>Aging images

Older images present a higher security risk because they can contain vulnerabilities that have already been addressed. If older images are active, they can expose deployments to exploits. You can use this widget to quickly assess your security posture and identify offending images. You can use the default ranges or customize the age intervals with your own values. You can view both inactive and active images or use the Dashboard filter to focus on a particular area for active images. You can then click on an age group in this widget to view only those images in the Vulnerability

Management → Images page.

<a name="_page4_x39.00_y56.25"></a>Policy violations by category

This widget can help you gain insights about the challenges your organization is facing in complying with security policies, by analyzing which types of policies are violated more than others. The widget shows the five policy categories of highest interest. Explore the Options menu for different ways to slice the data. You can filter the data to focus exclusively on deploy or runtime violations.

You can also change the sorting mode. By default, the data is sorted by the number of violations within the highest severity first. Therefore, all categories with critical policies will appear before categories without critical policies. The other sorting mode considers the total number of violations regardless of severity. Because some categories contain no critical policies (for example, “Docker CIS”), the two sorting modes can provide significantly different views, offering additional insight.

Click on a severity level at the bottom of the graph to include or exclude that level from the data. Selecting different severity levels can result in a different top five selection or ranking order. Data is filtered to the scope selected by the Dashboard filter.

<a name="_page4_x39.00_y423.00"></a>Compliance by standard

You can use the Compliance by standard widget with the Dashboard filter to focus on areas that matter to you the most. The widget lists the top or bottom six compliance benchmarks, depending on sort order. Select Options to sort by the coverage percentage. Click on one of the benchmark labels or graphs to go directly to the Compliance Controls page, filtered by the Dashboard scope and the selected benchmark.

- The Compliance widget shows details only after you run a com[pliance scan.](https://docs.openshift.com/acs/4.4/operating/manage-compliance/managing-compliance-10.html#run-compliance-scan_managing-compliance-10)![ref1]![ref2]
https://docs.openshift.com/acs/4.4/operating/view-dashboard.html 5/5

[ref1]: Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.007.png
[ref2]: Aspose.Words.85312192-a209-4b3e-b0a0-1f4adc319311.008.png


6/5/24, 2:28 PM Upgrading using the Operator | Upgrading | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.001.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.002.png)

Upgrading by using the Operator

- [Preparing to upgrade](#_page1_x39.00_y204.00)
  - [Changing the collection method](#_page1_x39.00_y449.25)
  - [Setting the forceCollection parameter](#_page2_x39.00_y282.00)
- [Modifying Central custom resource](#_page3_x39.00_y56.25)
- [Modifying Central custom resource for external database](#_page3_x39.00_y548.25)
- [Changing subscription channel](#_page5_x39.00_y408.75)
- [Removing Central-attached PV after upgrading to version 4.1 and later](#_page7_x39.00_y139.50)
  - [Removing Central-attached PV using the RHACS Operator for RHACS version 4.1 and later](#_page7_x39.00_y534.75)
- [Rolling back an Operator upgrade](#_page8_x39.00_y198.75)
  - [Rolling back an Operator upgrade by using the CLI](#_page8_x39.00_y383.25)
  - [Rolling back an Operator upgrade by using the web console](#_page12_x39.00_y229.50)
- [Troubleshooting Operator upgrade issues](#_page14_x39.00_y627.75)
  - [Central DB cannot be scheduled](#_page15_x39.00_y56.25)
  - [Central or Secured cluster fails to deploy](#_page16_x39.00_y56.25)

Upgrades through the Red Hat Advanced Cluster Security for Kubernetes (RHACS) Operator are performed automatically or manually, depending on the Update approval option you chose at installation.

Follow these guidelines when upgrading:

- If the version for Central is earlier than 3.74, you must upgrade to 3.74 before upgrading to a 4.x version. For upgrading Central to version 3.74, see the upgra[de documentation for version 3.74.](https://access.redhat.com/documentation/en-us/red_hat_advanced_cluster_security_for_kubernetes/3.74/html/upgrading/index)
- When upgrading Operator-based Central deployments from version 3.74, first ensure the Operator upgrade mode is set to  Manual . Then, upgrade the Operator to version 4.0 following the procedure in the upgr[ade documentation for version 4.0 a](https://access.redhat.com/documentation/en-us/red_hat_advanced_cluster_security_for_kubernetes/4.0/html/upgrading/upgrade-operator)nd ensure that Central is online. After the upgrade to version 4.0 is complete, Red Hat recommends upgrading Central to the latest version for full functionality.

<a name="_page1_x39.00_y204.00"></a>Preparing to upgrade

Before you upgrade the Red Hat Advanced Cluster Security for Kubernetes (RHACS) version, you must perform the following steps:

- If you are upgrading from version 3.74, verify that you are running the latest patch release version of the RHACS Operator 3.74.
- Backup your existing Central database.
- If the cluster you are upgrading contains the  SecuredCluster custom resource (CR), change the collection method to EBPF or CORE\_BPF. For more information, see "Changing the collection method".

<a name="_page1_x39.00_y449.25"></a>Changing the collection method

If the cluster that you are upgrading contains the  SecuredCluster CR, you must ensure that the per node collection setting is set to  CORE\_BPF before you upgrade, if you are upgrading from 4.1 or later. Otherwise, set the collection method to  EBPF . To set the collection method to  EBPF , you must set the  forceCollection parameter to

true after the upgrade and make sure that the collection method is  EBPF .

Procedure

- In the OpenShift Container Platform web console, go to the RHACS Operator page.
- In the top navigation menu, select Secured Cluster .
- Click the instance name, for example, stackrox-secured-cluster-services .
- Use one of the following methods to change the setting:
- In the Form view, under Per Node Settings → Collector Settings → Collection , select CORE\_BPF .
- Click YAML to open the YAML editor and locate the

  spec.perNode.collector.collection attribute. If the value is KernelModule , then change it to  CORE\_BPF .

- Only use  EBPF if you are upgrading from a version earlier ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.003.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.004.png)than 4.1 or if there is a specific reason to use it.
- Click Save.

<a name="_page2_x39.00_y282.00"></a>Setting the forceCollection parameter

When upgrading secured clusters, if you set the collection method to  EBPF , you must set the  forceCollection parameter to  true after the upgrade. Then, make sure that the  spec.perNode.collector.collection is still set to  EBPF in the YAML editor.

Procedure

- In the OpenShift Container Platform web console, go to the RHACS Operator page.
- In the top navigation menu, select Secured Cluster .
- Click the instance name, for example, stackrox-secured-cluster-services .
- Click YAML to open the YAML editor.
- Locate the  spec.perNode.collector.forceCollection parameter and set it to  true .
- Click Save.

Additional resources

- [Updating installed Operators](https://docs.openshift.com/container-platform/latest/operators/admin/olm-upgrading-operators.html)
- [Backing up Red Hat Advanced Cluster Security for Kubernetes](https://docs.openshift.com/acs/4.4/backup_and_restore/backing-up-acs.html#backing-up-acs)

<a name="_page3_x39.00_y56.25"></a>Modifying Central custom resource

The Central DB service requires persistent storage. If you have not configured a default storage class for the Central cluster that is an SSD or is high performance, you must update the  Central custom resource to configure the storage class for the Central DB persistent volume claim (PVC).

- Skip this section if you have already configured a default storage class ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.005.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.006.png)for Central.

Procedure

- Update the central custom resource with the following configuration:

spec:

`  `central:

`    `db:

`      `isEnabled: Default  **(1)**

`      `persistence:

`        `persistentVolumeClaim:  **(2)**

`          `claimName: central-db

`          `size: 100Gi

`          `storageClassName: <storage-class-name>

1 You must not change the value of  IsEnabled to  Enabled .

If this claim exists, your cluster uses the existing claim, otherwise it creates a new 2

claim.

<a name="_page3_x39.00_y548.25"></a>Modifying Central custom resource for external database

Prerequisites

- You must have a database in your database instance that supports PostgreSQL 13 and a user with the following permissions:
  - Connection rights to the database.
  - Usage and  Create on the schema.
  - Select ,  Insert ,  Update , and  Delete on all tables in the schema.
- Usage on all sequences in the schema.

Procedure

- Create a password secret in the deployed namespace by using the OpenShift Container Platform web console or the terminal.
  - On the OpenShift Container Platform web console, go to the Workloads
    - Secrets page. Create a Key/Value secret with the key  password and the value as the path of a plain text file containing the password for the superuser of the provisioned database.
  - Or, run the following command in your terminal:

    $ oc create secret generic external-db-password \ **(1) ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.007.png)**  --from-file=password=<password.txt> **(2)**

    1 If you use Kubernetes, enter  kubectl instead of  oc .

    Replace  password.txt with the path of the file which has the plain text 2

password.

- Go to the Red Hat Advanced Cluster Security for Kubernetes operator page in the OpenShift Container Platform web console. Select Central in the top navigation bar and select the instance you want to connect to the database.
- Go to the YAML editor view.
- For  **db.passwordSecret.name** specify the referenced secret that you created in earlier steps. For example,  external-db-password .
- For  **db.connectionString** specify the connection string in  keyword=value format, for example,  host=<host> port=5432 database=stackrox

  user=stackrox sslmode=verify-ca

- For  **db.persistence** delete the entire block.
- If necessary, you can specify a Certificate Authority for Central to trust the database certificate by adding a TLS block under the top-level spec, as shown in the following example:
  - Update the central custom resource with the following configuration:

    spec:![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.008.png)

    `  `tls:

    `    `additionalCAs:

- name: db-ca

`      `content: |

`        `<certificate>

`  `central:

`    `db:

`      `isEnabled: Default **(1)**

`      `connectionString: "host=<host> port=5432 user=<user> sslmode=verify-ca"

`      `passwordSecret:

`        `name: external-db-password

1 You must not change the value of  IsEnabled to  Enabled .

- Click Save .

Additional resources

- [Provisioning a database in your PostgreSQL instance](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#provision-postgresql-database_install-central-ocp)

<a name="_page5_x39.00_y408.75"></a>Changing subscription channel

You can change the update channel for the RHACS Operator by using the OpenShift Container Platform web console or by using the command line. For upgrading to RHACS 4.0 from RHACS 3.74, you must change the update channel.

You must change the subscription channel for all clusters where you![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.009.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.010.png)

j have installed RHACS Operator, including Central and all Secured clusters.

Prerequisites

- You must verify that you are using the latest RHACS 3.74 Operator and there are no pending manual Operator upgrades.
- You must verify that you have backed up your existing Central database.
- You have access to an OpenShift Container Platform cluster web console using an account with  cluster-admin permissions.

Changing the subscription channel by using the web console

Use the following instructions for changing the subscription channel by using the web console:

Procedure

- In the Administrator perspective of the OpenShift Container Platform web console, go to Operators → Installed Operators .
- Locate the RHACS Operator and click on it.
- Click the Subscription tab.
- Click the name of the update channel under Update Channel.
- Select stable , then click Save .
- For subscriptions with an Automatic approval strategy, the update begins automatically. Go back to the Operators → Installed Operators page to monitor the progress of the update. When complete, the status changes to Succeeded and Up to date .

  For subscriptions with a Manual approval strategy, you can manually approve the update from the Subscription tab.

Changing the subscription channel by using command line

Use the following instructions for changing the subscription channel by using command line:

Procedure

- Run the following command to change the subscription channel to  stable :

$ oc -n rhacs-operator \ **(1)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.011.png)**

`  `patch subscriptions.operators.coreos.com rhacs-operator \   --type=merge --patch='{ "spec": { "channel": "stable" }}'

1 If you use Kubernetes, enter  kubectl instead of  oc .

During the update the RHACS Operator provisions a new deployment called  central - db and your data begins migrating. It takes around 30 minutes and only happens once when you upgrade.

<a name="_page7_x39.00_y139.50"></a>Removing Central-attached PV after upgrading to version 4.1 and later

Kubernetes and OpenShift Container Platform do not delete persistent volumes (PV) automatically. When you upgrade RHACS from earlier versions, the Central PV called

stackrox-db remains mounted. However, in RHACS 4.1, Central does not need the previously attached PV anymore.

The PV has data and persistent files used by earlier RHACS versions. You can use the PV to roll back to an earlier version before RHACS 4.1. Or, if you have a large RocksDB backup bundle for Central, you can use the PV to restore that data.

After you complete the upgrade to 4.1, you can remove the Central-attached persistent volume claim (PVC) to free up the storage. Only remove the PVC if you do not plan to roll back or restore from earlier RocksDB backups.

After removing PVC, you cannot roll back Central to an earlier version![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.012.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.013.png)

q before RHACS 4.1 or restore large RocksDB backups created with RocksDB.

<a name="_page7_x39.00_y534.75"></a>Removing Central-attached PV using the RHACS Operator for RHACS version 4.1 and later

Remove the Central-attached persistent volume claim (PVC)  stackrox-db to free up storage space.

Procedure

- Add the following annotation to Central:

annotations:![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.014.png)

`  `platform.stackrox.io/obsolete-central-pvc: "true"

Verification

- Run the following command:

$ oc -n stackrox describe pvc stackrox-db | grep -i 'Used By' Used By: <none> ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.015.png)**(1)**

1 Wait until you see  Used By: <none> . It might take a few minutes.

<a name="_page8_x39.00_y198.75"></a>Rolling back an Operator upgrade

To roll back an Operator upgrade, you must perform the steps described in one of the following sections. You can roll back an Operator upgrade by using the CLI or the OpenShift Container Platform web console.

- If you are rolling back from RHACS 4.0, you can only rollback to the ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.016.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.017.png)latest patch release version of RHACS 3.74.

<a name="_page8_x39.00_y383.25"></a>Rolling back an Operator upgrade by using the CLI

You can roll back the Operator version by using CLI commands. Procedure

- Delete the OLM subscription by running the following command:
  - For OpenShift Container Platform, run the following command:

    $ oc -n rhacs-operator delete subscription rhacs-operator![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.018.png)

- For Kubernetes, run the following command:

  $ kubectl -n rhacs-operator delete subscription rhacs- operator![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.019.png)

- Delete the cluster service version (CSV) by running the following command:
  - For OpenShift Container Platform, run the following command:

    $ oc -n rhacs-operator delete csv -l operators.coreos.com/rhacs-operator.rhacs-operator![ref1]

- For Kubernetes, run the following command:

  $ kubectl -n rhacs-operator delete csv -l operators.coreos.com/rhacs-operator.rhacs-operator![ref1]

- Determine the previous version you want to roll back to by choosing one of the following options:
  - If the current Central instance is running, query the RHACS API to get the rollback version by running the following command:

    $ curl -k -s -u <user>:<password> https://<central hostname>/v1/centralhealth/upgradestatus | jq -r .upgradeStatus.forceRollbackTo![ref2]

- If the current Central instance is not running, perform the following steps:
- This procedure can only be used for RHACS release 3.74 ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.022.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.023.png)and earlier when the  rocksdb database is installed.
- Ensure the Central deployment is scaled down by running the following command:
  - For OpenShift Container Platform, run the following command:

    $ oc scale -n <central namespace> –replicas=0 deploy/central![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.024.png)

- For Kubernetes, run the following command:

  $ kubectl scale -n <central namespace> –replicas=0 deploy/central![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.025.png)

- Save the following pod spec as a YAML file:

  apiVersion: v1![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.026.png)

  kind: Pod

  metadata:

  `  `name: get-previous-db-version

  spec:

  `  `containers:

- name: get-previous-db-version

`    `image: registry.redhat.io/advanced-cluster- security/rhacs-main-rhel8:<rollback version>

`    `command:

- sh

`    `args:

- '-c'
- "cat 

/var/lib/stackrox/.previous/migration\_version.yaml | grep '^image:' | cut -f 2 -d : | tr -d ' '"

`    `volumeMounts:

- name: stackrox-db

`      `mountPath: /var/lib/stackrox

`  `volumes:

- name: stackrox-db

`    `persistentVolumeClaim:

`      `claimName: stackrox-db

- Create a pod in your Central namespace by running the following command using the YAML file that you saved:
  - For OpenShift Container Platform, run the following command:

    $ oc create -n <central namespace> -f pod.yaml![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.027.png)

- For Kubernetes, run the following command:

  $ kubectl create -n <central namespace> -f pod.yaml![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.028.png)

- After pod creation is complete, get the version by running the following command:
  - For OpenShift Container Platform, run the following command:

    $ oc logs -n <central namespace> get-previous-db- version![ref3]

- For Kubernetes, run the following command:

  $ kubectl logs -n <central namespace> get-previous- db-version![ref3]

- Edit the  central-config.yaml ConfigMap to set the maintenance.forceRollBackVersion:<version> parameter by running the

  following command:

- For OpenShift Container Platform, run the following command:

  $ oc get configmap -n <central namespace> central-config -o yaml | sed -e "s/forceRollbackVersion: none/forceRollbackVersion: <version>/" | oc -n <central namespace> apply -f -![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.030.png)

- For Kubernetes, run the following command:

  $ kubectl get configmap -n <central namespace> central-config -o yaml | sed -e "s/forceRollbackVersion: none/forceRollbackVersion: <version>/" | kubectl -n <central namespace> apply -f -![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.031.png)

- Set the image for the Central deployment using the version string shown in Step 3 as the image tag. For example, run the following command:
  - For OpenShift Container Platform, run the following command:

    $ oc set image -n <central namespace> deploy/central central=registry.redhat.io/advanced-cluster-security/rhacs- main-rhel8:<version>![ref2]

- For Kubernetes, run the following command:

  $ kubectl set image -n <central namespace> deploy/central central=registry.redhat.io/advanced-cluster-security/rhacs- main-rhel8:<version>![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.032.png)

Verification

- Ensure that the Central pod starts and has a  ready status. If the pod crashes, check the logs to see if the backup was restored. A successful log message appears similar to the following example:

Clone to Migrate ".previous", ""

- Reinstall the Operator on the rolled back channel. For example,  3.74.2 is installed on the  rhacs-3.74 channel.

<a name="_page12_x39.00_y229.50"></a>Rolling back an Operator upgrade by using the web console

You can roll back the Operator version by using the OpenShift Container Platform web console.

Prerequisites

- You have access to an OpenShift Container Platform cluster web console using an account with  cluster-admin permissions.

Procedure

- Go to the Operators → Installed Operators page.
- Locate the RHACS Operator and click on it.
- On the Operator Details page, select Uninstall Operator from the Actions list. Following this action, the Operator stops running and no longer receives updates.
- Determine the previous version you want to roll back to by choosing one of the following options:
  - If the current Central instance is running, you can query the RHACS API to get the rollback version by running the following command from a terminal window:

    $ curl -k -s -u <user>:<password> https://<central hostname>/v1/centralhealth/upgradestatus | jq -r .upgradeStatus.forceRollbackTo![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.033.png)

- You can create a pod and extract the previous version by performing the following steps:
- This procedure can only be used for RHACS release 3.74 ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.034.png)![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.035.png)and earlier when the  rocksdb database is installed.
- Go to Workloads → Deployments → central.
- Under Deployment details , click the down arrow next to the pod count to scale down the pod.
- Go to Workloads → Pods → Create Pod and paste the contents of the pod spec as shown in the following example into the editor:

  apiVersion: v1![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.036.png)

  kind: Pod

  metadata:

  `  `name: get-previous-db-version

  spec:

  `  `containers:

- name: get-previous-db-version

`    `image: registry.redhat.io/advanced-cluster- security/rhacs-main-rhel8:<rollback version>

`    `command:

- sh

`    `args:

- '-c'
- "cat 

/var/lib/stackrox/.previous/migration\_version.yaml | grep '^image:' | cut -f 2 -d : | tr -d ' '"

`    `volumeMounts:

- name: stackrox-db

`      `mountPath: /var/lib/stackrox

`  `volumes:

- name: stackrox-db

`    `persistentVolumeClaim:

`      `claimName: stackrox-db

- Click Create .
  - After the pod is created, click the Logs tab to get the version string.
- Update the rollback configuration by performing the following steps:
  - Go to Workloads → ConfigMaps → central-config and select Edit ConfigMap from the Actions list.
  - Find the  forceRollbackVersion line in the value of the  central - config.yaml key.
  - Replace  none with  3.73.3 , and then save the file.
- Update Central to the earlier version by performing the following steps:
  - Go to Workloads → Deployments → central and select Edit Deployment from the Actions list.
  - Update the image name, and then save the changes.

Verification

- Ensure that the Central pod starts and has a  ready status. If the pod crashes, check the logs to see if the backup was restored. A successful log message appears similar to the following example:

Clone to Migrate ".previous", ""

- Reinstall the Operator on the rolled back channel. For example,  3.74.2 is installed on the  rhacs-3.74 channel.

Additional resources

- [Installing Central using the Operator method](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-operator_install-central-ocp)
- [Operator Lifecycle Manager workflow](https://access.redhat.com/documentation/en-us/openshift_container_platform/4.15/html/operators/understanding-operators#olm-workflow)
- [Manually approving a pending Operator update](https://access.redhat.com/documentation/en-us/openshift_container_platform/4.15/html/operators/administrator-tasks#olm-approving-pending-upgrade_olm-upgrading-operators)

<a name="_page14_x39.00_y627.75"></a>Troubleshooting Operator upgrade issues

Follow these instructions to investigate and resolve upgrade-related issues for the RHACS Operator.

<a name="_page15_x39.00_y56.25"></a>Central DB cannot be scheduled

Follow the instructions here to troubleshoot a failing Central DB pod during an upgrade:

- Check the status of the  central-db pod:

$ oc -n <namespace> get pod -l app=central-db **(1)![ref4]**

1 If you use Kubernetes, enter  kubectl instead of  oc .

- If the status of the pod is  Pending , use the describe command to get more details:

  $ oc -n <namespace> describe po/<central-db-pod-name> **(1) ![ref4]**1 If you use Kubernetes, enter  kubectl instead of  oc .

- You might see the  FailedScheduling warning message:

Type     Reason            Age   From               Message![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.038.png)

----     ------            ----  ----               ------- Warning  FailedScheduling  54s   default-scheduler  0/7 nodes are available: 1 Insufficient memory, 3 node(s) had untolerated taint {node-role.kubernetes.io/master: }, 4 Insufficient cpu. preemption: 0/7 nodes are available: 3 Preemption is not helpful for scheduling, 4 No preemption victims found for incoming pod.

- This warning message suggests that the scheduled node had insufficient memory to accommodate the pod’s resource requirements. If you have a small environment, consider increasing resources on the nodes or adding a larger node that can support the database.

  Otherwise, consider decreasing the resource requirements for the  central-db pod in the custom resource under  central →  db →  resources . However, running central with fewer resources than the recommended minimum might lead to degraded performance for RHACS.

<a name="_page16_x39.00_y56.25"></a>Central or Secured cluster fails to deploy

When RHACS Operator:

- fails to deploy Central or Secured Cluster.
- fails to apply CR changes to actual resources.

You must check the custom resource conditions to find the issue.

- For Central, run the following command to check the conditions:

  $ oc -n rhacs-operator describe centrals.platform.stackrox.io **(1) ![ref4]**1 If you use Kubernetes, enter  kubectl instead of  oc .

- For Secured clusters, run the following command to check the conditions:

$ oc -n rhacs-operator describe securedclusters.platform.stackrox.io ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.039.png)**(1)**

1 If you use Kubernetes, enter  kubectl instead of  oc . You can identify configuration errors from the conditions output: Example output

` `Conditions:![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.040.png)

`    `Last Transition Time:  2023-04-19T10:49:57Z

`    `Status:                False

`    `Type:                  Deployed

`    `Last Transition Time:  2023-04-19T10:49:57Z

`    `Status:                True

`    `Type:                  Initialized

`    `Last Transition Time:  2023-04-19T10:59:10Z

`    `Message:               Deployment.apps "central" is invalid: spec.template.spec.containers[0].resources.requests: Invalid value: "50": must be less than or equal to cpu limit

`    `Reason:                ReconcileError

`    `Status:                True

`    `Type:                  Irreconcilable

`    `Last Transition Time:  2023-04-19T10:49:57Z

`    `Message:               No proxy configuration is desired

`    `Reason:                NoProxyConfig

`    `Status:                False

`    `Type:                  ProxyConfigFailed

`    `Last Transition Time:  2023-04-19T10:49:57Z

`    `Message:               Deployment.apps "central" is invalid: spec.template.spec.containers[0].resources.requests: Invalid value: "50": must be less than or equal to cpu limit

`    `Reason:                InstallError

`    `Status:                True

`    `Type:                  ReleaseFailed

Additionally, you can view RHACS pod logs to find more information about the issue. Run the following command to view the logs:

oc -n rhacs-operator logs deploy/rhacs-operator-controller-manager manager ![](Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.041.png)**(1)**

1 If you use Kubernetes, enter  kubectl instead of  oc .
https://docs.openshift.com/acs/4.4/upgrading/upgrade-operator.html 18/18

[ref1]: Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.020.png
[ref2]: Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.021.png
[ref3]: Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.029.png
[ref4]: Aspose.Words.7ecbeb1a-b174-41f6-9a46-22ea0cfb260e.037.png


6/5/24, 2:27 PM RHACS architecture | Architecture | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.001.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.002.png)

Red Hat Advanced Cluster Security for Kubernetes architecture

- [Red Hat Advanced Cluster Security for Kubernetes architecture overview](#_page0_x39.00_y441.00)
- [Central services](#_page3_x39.00_y218.25)
  - [Vulnerability sources](#_page5_x39.00_y319.50)
- [Secured cluster services](#_page6_x39.00_y467.25)
- [External components](#_page8_x39.00_y296.25)
- [Architectural differences between installation on OpenShift Container Platform and Kubernetes](#_page9_x39.00_y139.50)
- [Interaction between the services](#_page11_x39.00_y56.25)

Discover Red Hat Advanced Cluster Security for Kubernetes architecture and concepts.

<a name="_page0_x39.00_y441.00"></a>Red Hat Advanced Cluster Security for Kubernetes architecture overview

Red Hat Advanced Cluster Security for Kubernetes (RHACS) uses a distributed architecture that supports high-scale deployments and is optimized to minimize the impact on the underlying OpenShift Container Platform or Kubernetes nodes.

The architecture is slightly different when you install RHACS on![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.003.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.004.png)

- Kubernetes and in OpenShift Container Platform. However, the underlying components and the interactions between them remain the same.

RHACS architecture for Kubernetes

The following graphic shows the architecture with the StackRox Scanner. For version 4.4, Scanner V4 is available. Installation of Scanner V4 is optional, but provides additional benefits.

Scanner V4 is a Technology Preview feature only. Technology Preview ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.005.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.006.png)features are not supported with Red Hat production service level agreements (SLAs) and might not be functionally complete. Red Hat does not recommend using them in production. These features provide

- early access to upcoming product features, enabling customers to test functionality and provide feedback during the development process.

  For more information about the support scope of Red Hat Technology Preview features, see Te[chnology Preview Features Support Scope.](https://access.redhat.com/support/offerings/techpreview/)

![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.007.jpeg)

You install RHACS as a set of containers in your OpenShift Container Platform or Kubernetes cluster. RHACS includes the following services:

- Central services you install on one cluster
- Secured cluster services you install on each cluster you want to secure by RHACS

In addition to these primary services, RHACS also interacts with other external components to enhance your clusters' security.

Additional resources

- [Architectural differences between installation on OpenShift Container Platform and Kubernetes](#_page9_x39.00_y139.50)
- [External components](#_page8_x39.00_y296.25)

<a name="_page3_x39.00_y218.25"></a>Central services

You install Central services on a single cluster. These services include the following components:

- Central: Central is the RHACS application management interface and services. It handles API interactions and user interface (RHACS Portal) access. You can use the same Central instance to secure multiple OpenShift Container Platform or Kubernetes clusters.
- Central DB : Central DB is the database for RHACS and handles all data persistence. It is currently based on PostgreSQL 13.
- Scanner V4 (Technology Preview): Beginning with version 4.4, RHACS contains the Scanner V4 vulnerability scanner for scanning container images. Scanner V4 is built on [ClairCore, ](https://github.com/quay/claircore)which also powers the Cl[air sc](https://github.com/quay/clair)anner. Scanner V4 supports scanning of language and OS-specific image components. For version 4.4, you must use this scanner in conjunction with the StackRox Scanner to provide node and platform scanning capabilities until Scanner V4 support those capabilities. Scanner V4 contains the Indexer, Matcher, and DB components.

Scanner V4 is a Technology Preview feature only. Technology Preview ![ref1]![ref2]features are not supported with Red Hat production service level agreements (SLAs) and might not be functionally complete. Red Hat does not recommend using them in production. These features provide early access to upcoming

- product features, enabling customers to test functionality and provide feedback during the development process.

  For more information about the support scope of Red Hat Technology Preview features, see Te[chnology Preview Features Support Scope.](https://access.redhat.com/support/offerings/techpreview/)

- Scanner V4 Indexer : The Scanner V4 Indexer performs image indexing, previously known as image analysis. Given an image and registry credentials, the Indexer pulls the image from the registry. It finds the base operating system, if it exists, and looks for packages. It stores and outputs an index report, which contains the findings for the given image.
- Scanner V4 Matcher : The Scanner V4 Matcher performs vulnerability matching. If the Central services Scanner V4 Indexer indexed the image, then the Matcher fetches the index report from the Indexer and matches the report with the vulnerabilities stored in the Scanner V4 database. If a Secured Cluster services Scanner V4 Indexer performed the indexing, then the Matcher uses the index report that was sent from that Indexer, and then matches against vulnerabilities. The Matcher also fetches vulnerability data and updates the Scanner V4 database with the latest vulnerability data. The Scanner V4 Matcher outputs a vulnerability report, which contains the final results of an image.
- Scanner V4 DB : This database stores information for Scanner V4, including all vulnerability data and index reports. A persistent volume claim (PVC) is required for Scanner V4 DB on the cluster where Central is installed.
- StackRox Scanner : The StackRox Scanner is the default scanner in RHACS. Version 4.4 adds a new scanner, Scanner V4. The StackRox Scanner originates from a fork of the Clair v2 open source scanner. You must continue using this scanner for RHCOS node scanning and platform scanning.
- Scanner-DB: This database contains data for the StackRox Scanner.

RHACS scanners analyze each image layer to determine the base operating system and identify programming language packages and packages that were installed by the operating system package manager. They match the findings against known vulnerabilities from various vulnerability sources. In addition, the StackRox Scanner identifies vulnerabilities in the node’s operating system and platform. These capabilities are planned for Scanner V4 in a future release.

<a name="_page5_x39.00_y319.50"></a>Vulnerability sources

RHACS uses the following vulnerability sources:

- [Alpine Security Database](https://secdb.alpinelinux.org/)
- Data tracked in [Amazon Linux Security Center](https://alas.aws.amazon.com/index.html)
- [Debian Security Tracker](https://security-tracker.debian.org/tracker/data/json)
- [Oracle OVAL](https://linux.oracle.com/security/oval)
- [Photon OVAL](https://packages.vmware.com/photon/photon_oval_definitions/)
- [Red Hat OVAL](https://access.redhat.com/security/data/oval/v2/)
- [Red Hat CVE Map:](https://access.redhat.com/security/data/metrics/cvemap.xml) This is used for images which appear in the Red[ Hat Container Catalog.](https://catalog.redhat.com/software/containers/explore)
- [SUSE OVAL](https://support.novell.com/security/oval/)
- [Ubuntu OVAL](https://security-metadata.canonical.com/oval/)
- [OSV:](https://osv.dev/) This is used for language-related vulnerabilities, such as Go, Java, Node.js (JavaScript), Python, and Ruby. This source might provide GitHub Security Advisory (GHSA) IDs rather than CVE numbers for vulnerabilities.
- The RHACS Scanner V4 uses the OSV database available at ![ref3]![ref4][OSV.dev ](https://osv.dev/)under t[his license.](https://github.com/google/osv.dev/blob/master/LICENSE)
- [NVD](https://nvd.nist.gov/vuln/search): This used for various purposes such as filling in information gaps when vendors do not provide information. For example, Alpine does not provide a description, CVSS score, severity, or published date.
- This product uses the NVD API but is not endorsed or certified by ![ref3]![ref4]the NVD.
- [StackRox:](https://github.com/stackrox/stackrox/blob/master/scanner/updater/manual/vulns.go) The upstream StackRox project maintains a set of vulnerabilities that might not be discovered due to data formatting from other sources or absence of data.

The Scanner V4 Indexer uses the following sources:

- [repository-to-cpe.json: M](https://www.redhat.com/security/data/metrics/repository-to-cpe.json)aps RPM repositories to their related CPEs, which is required for matching vulnerabilities for RHEL-based images.
- [container-name-repos-map.json: Th](https://access.redhat.com/security/data/metrics/container-name-repos-map.json)is matches container names to the repositories to which they are shipped.

<a name="_page6_x39.00_y467.25"></a>Secured cluster services

You install the secured cluster services on each cluster that you want to secure by using the RHACS Cloud Service. Secured cluster services include the following components:

- Sensor : Sensor is the service responsible for analyzing and monitoring the cluster. Sensor listens to the OpenShift Container Platform or Kubernetes API and Collector events to report the current state of the cluster. Sensor also triggers deploy-time and runtime violations based on RHACS Cloud Service policies. In addition, Sensor is responsible for all cluster interactions, such as applying network policies, initiating reprocessing of RHACS Cloud Service policies, and interacting with the Admission controller.
- Admission controller : The Admission controller prevents users from creating workloads that violate security policies in RHACS Cloud Service.
- Collector : Collector analyzes and monitors container activity on cluster nodes. It collects container runtime and network activity information and sends the collected data to Sensor.
- StackRox Scanner : In Kubernetes, the secured cluster services include Scanner- slim as an optional component. However, on OpenShift Container Platform, RHACS Cloud Service installs a Scanner-slim version on each secured cluster to scan images in the OpenShift Container Platform integrated registry and optionally other registries.
- Scanner-DB: This database contains data for the StackRox Scanner.
- Scanner V4 : Scanner V4 components are installed on the secured cluster if enabled.

Scanner V4 is a Technology Preview feature only. Technology Preview ![ref1]![ref2]features are not supported with Red Hat production service level agreements (SLAs) and might not be functionally complete. Red Hat does not recommend using them in

- production. These features provide early access to upcoming product features, enabling customers to test functionality and provide feedback during the development process.

  For more information about the support scope of Red Hat Technology Preview features, see Te[chnology Preview Features Support Scope.](https://access.redhat.com/support/offerings/techpreview/)

- Scanner V4 Indexer : The Scanner V4 Indexer performs image indexing, previously known as image analysis. Given an image and registry credentials, the Indexer pulls the image from the registry. It finds the base operating system, if it exists, and looks for packages. It stores and outputs an index report, which contains the findings for the given image.
- Scanner V4 DB : This component is installed if Scanner V4 is enabled. This database stores information for Scanner V4, including index reports. For best performance, configure a persistent volume claim (PVC) for Scanner V4 DB.

When secured cluster services are installed on the same ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.012.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.013.png)cluster as Central services and installed in the same

- namespace, secured cluster services do not deploy Scanner V4 components. Instead, it is assumed that Central services

  already include a deployment of Scanner V4.

<a name="_page8_x39.00_y296.25"></a>External components

Red Hat Advanced Cluster Security for Kubernetes (RHACS) interacts with the following external components:

- Third-party systems : You can integrate RHACS with other systems such as CI/CD pipelines, event management (SIEM) systems, logging, email, and more.
- **roxctl** :  roxctl is a command-line interface (CLI) for running commands on

  RHACS.

- Image registries : You can integrate RHACS with various image registries and use RHACS to scan and view images. RHACS automatically configures registry integrations for active images by using the image pull secrets discovered in secured clusters. However, for scanning inactive images, you must manually configure registry integrations.
- **definitions.stackrox.io** : RHACS aggregates the data from various vulnerability feeds at the  definitions.stackrox.io endpoint and passes this information to Central. The feeds include general, National Vulnerability Database (NVD) data, and distribution-specific data, such as Alpine, Debian, and Ubuntu.
- **collector-modules.stackrox.io** : Central reaches out to  collector - modules.stackrox.io to obtain supported kernel modules and passes on these

  modules to Collector.

<a name="_page9_x39.00_y139.50"></a>Architectural differences between installation on OpenShift Container Platform and Kubernetes

When you install RHACS on the OpenShift Container Platform, there are only two architectural differences:

- RHACS installs a lightweight version of Scanner on every secured cluster when you install RHACS on the OpenShift Container Platform using the Operator or the Helm install method. The lightweight Scanner enables the scanning of images in the integrated OpenShift Container Registry (OCR).
- Sensor communicates with Scanner in the cluster where you have installed Central. This connection allows accessing internal registries attached to the cluster.

![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.014.jpeg)

Figure 1. Red Hat Advanced Cluster Security for Kubernetes architecture for OpenShift Container Platform

<a name="_page11_x39.00_y56.25"></a>Interaction between the services

This section explains how RHACS services interact with each other.

*Table 1. RHACS with Scanner V4*

Directio ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.015.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.016.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.017.png)

Component n Component Description

Central ⮂ Scanner V4 Indexer Central requests the Indexer to download and

index (analyze) given images. This process results in an index report. Scanner V4 Indexer requests mapping files from Central that assist the indexing process.

Central ⮂ Scanner V4 Matcher Central requests that the Scanner V4![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.018.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.019.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.020.png)

Matcher match given images to known vulnerabilities. This process results in the final scan result: a vulnerability report. Scanner V4 Matcher requests the latest vulnerabilities from Central.

Sensor ⮂ Scanner V4 Indexer SecuredCluster scanning is enabled by ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.021.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.022.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.023.png)default in Red Hat OpenShift environments

deployed by using the Operator or when delegated scanning is used. When SecuredCluster scanning is enabled,

Sensor requests Scanner V4 to index images. Scanner V4 Indexer requests mapping files from Sensor that assist the indexing process unless Central exists in the same namespace. In that case, Central is contacted instead.

Scanner V4 Indexer → Image Registries The Indexer pulls image metadata from

registries to determine the layers of the image, and downloads each previously unindexed layer.

Directio ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.024.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.025.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.026.png)

Component n Component Description

Scanner V4 Matcher → Scanner V4 Indexer Scanner V4 Matcher requests the results of

the image indexing, the index report, from the Indexer. It then uses the report to determine relevant vulnerabilities. This interaction occurs only when the image is indexed in the Central cluster. This interaction does not occur when Scanner V4 is matching vulnerabilities for images indexed in secured clusters.

Scanner V4 Indexer → Scanner V4 DB The Indexer stores data related to the

indexing results to ensure that image layers are only downloaded and indexed once. This prevents unnecessary network traffic and other resource utilization.

Scanner V4 Matcher → Scanner V4 DB Scanner V4 Matcher stores all of its

vulnerability data in the database and periodically updates this data. Scanner V4 indexer also queries this data as part of the vulnerability matching process.

Sensor ⮂ Central There is bidirectional communication![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.027.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.028.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.029.png)

between Central and Sensor. Sensor polls Central periodically to download updates for the sensor bundle configuration. It also sends events for the observed activity for the secured cluster and observed policy violations. Central communicates with Sensor to force reprocessing of all deployments against enabled policies.

Directio

Component n Component Description![ref5]![ref6]![ref7]

Collector ⮂ Sensor Collector communicates with Sensor and

sends all of the events to the respective Sensor for the cluster. On supported OpenShift Container Platform clusters, Collector analyzes the software packages installed on the nodes and sends them to Sensor so that Scanner can later scan them for vulnerabilities. Collector also requests missing drivers from Sensor. Sensor requests compliance scan results from Collector. Additionally, Sensor receives external Classless Inter-Domain Routing information from Central and pushes it to Collector.![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.033.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.034.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.035.png)

Admission controller ⮂ Sensor Sensors send the list of security policies to

enforce to Admission controller. Admission controller sends security policy violation alerts to Sensor. Admission controller can also request image scans from Sensor when required.![ref5]![ref6]![ref7]

Admission controller ➞ Central It is not common; however, Admission

controller can communicate with Central directly if the Central endpoint is known and Sensor is unavailable.

Scanner V4 is a Technology Preview feature only. Technology Preview ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.036.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.037.png)features are not supported with Red Hat production service level agreements (SLAs) and might not be functionally complete. Red Hat does not recommend using them in production. These features provide

- early access to upcoming product features, enabling customers to test functionality and provide feedback during the development process.

  For more information about the support scope of Red Hat Technology Preview features, see Te[chnology Preview Features Support Scope.](https://access.redhat.com/support/offerings/techpreview/)

*Table 2. RHACS with the StackRox Scanner*

Directio ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.038.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.039.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.040.png)

Component n Interacts with Description

Central ⮂ Scanner There is bidirectional communication

between Central and Scanner. Central requests image scans from Scanner, and Scanner requests updates to its CVE database from Central.

Central ➞ def i ni t i ons . s t ack Central connects to the

rox.io definitions.stackrox.io endpoint to

receive the aggregated vulnerability information.

Central ➞ col l ect or - Central downloads supported kernel modules

modules.stackrox. from  collector-modules.stackrox.io . io

Central ➞ Image registries Central queries the image registries to get

image metadata. For example, to show Dockerfile instructions in the RHACS portal.

Scanner ➞ Image registries Scanner pulls images from the image registry

to identify vulnerabilities.

Directio ![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.041.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.042.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.043.png)

Component n Interacts with Description

Sensor ⮂ Central There is bidirectional communication

between Central and Sensor. Sensor polls Central periodically for downloading updates for the sensor bundle configuration. It also sends events for the observed activity for the secured cluster and observed policy violations. Central communicates with Sensor to force reprocessing of all deployments against enabled policies.

Sensor ⮂ Scanner Only in OpenShift Container Platform,![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.044.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.045.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.046.png)

Sensor communicates with Scanner to access the local registry attached to the cluster. Scanner communicates with Sensor to request data from

definitions.stackrox.io .

Collector ⮂ Sensor Collector communicates with Sensor and![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.047.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.048.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.049.png)

sends all of the events to the respective Sensor for the cluster. On supported OpenShift Container Platform clusters, Collector analyzes the software packages installed on the nodes and sends them to Sensor so that Scanner can later scan them for vulnerabilities. Collector also requests missing drivers from Sensor. Sensor requests compliance scan results from Collector. Additionally, Sensor receives external Classless Inter-Domain Routing information from Central and pushes it to Collector.

Directio

Component n Interacts with Description![ref5]![ref6]![ref7]

Admission controller ⮂ Sensor Sensors send the list of security policies to

enforce to Admission controller. Admission controller sends security policy violation alerts to Sensor. Admission controller can also request image scans from Sensor when required.![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.050.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.051.png)![](Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.052.png)

Admission controller ➞ Central It is not common; however, Admission

controller can communicate with Central directly if the Central endpoint is known and Sensor is unavailable.
https://docs.openshift.com/acs/4.4/architecture/acs-architecture.html 17/17

[ref1]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.008.png
[ref2]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.009.png
[ref3]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.010.png
[ref4]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.011.png
[ref5]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.030.png
[ref6]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.031.png
[ref7]: Aspose.Words.577df58b-a8e3-485b-b21f-578bd116fd50.032.png

6/5/24, 2:28 PM Retrieving and analyzing the Collector logs and pod status | Troubleshooting Collector | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.001.png)![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.002.png)

Retrieving and analyzing the Collector logs and pod status

- [Retrieving the Collector logs](#_page0_x39.00_y405.00)
  - [Retrieving the logs with the  oc or  kubectl command](#_page0_x39.00_y555.75)
  - [Retrieving logs from a RHACS diagnostic bundle](#_page1_x39.00_y623.25)
- [Analyzing the Collector pod status](#_page2_x39.00_y56.25)

The first step in troubleshooting is to retrieve the logs and pods status. The logs allow you to identify the root cause of an error. In addition, examining the pod’s most recent status can provide information about failure messages.

<a name="_page0_x39.00_y405.00"></a>Retrieving the Collector logs

First, you should examine the logs from failing Collectors. Depending on your environment and access rights, you can obtain these logs in two ways:

- [Retrieving the logs with the  oc or  kubectl command](#_page0_x39.00_y555.75)
- [Retrieving logs from a RHACS diagnostic bundle](#_page1_x39.00_y623.25)

<a name="_page0_x39.00_y555.75"></a>Retrieving the logs with the oc or kubectl command

You can use either the  oc or  kubectl command to obtain logs from your running Collector pod. Optionally, you can even check the logs from a previous Collector pod if your current Collector pod is restarting.

Prerequisites

- Ensure that you have the authority to list the pods and logs:

$ oc auth can-i get pods && oc auth can-i get pods -- subresource=logs ![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.003.png)**(1)**

1 If you use Kubernetes, enter  kubectl instead of  oc . Procedure

- List all the pods with label  app=collector :

  $ oc get pods -n stackrox -l app=collector **(1) ![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.004.png)**1 If you use Kubernetes, enter  kubectl instead of  oc .

  Example output

collector-vclg5    1/2     CrashLoopBackOff   2 (25s ago)   2m41s+![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.005.png)

- Get the logs for the Collector pod:

$ oc logs -n stackrox *<collector\_pod\_name>* collector **(1)![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.006.png)**

If you use Kubernetes, enter  kubectl instead of  oc . For

1 *<collector\_pod\_name>*, specify the name of your Collector pod, for

example,  collector-vclg5 .

- (Optional) If the current Collector pod is restarting, you can check the logs for the previous Collector pod:

$ oc logs -n stackrox *<collector\_pod\_name>* collector --previous ![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.007.png)

**(1)**

If you use Kubernetes, enter  kubectl instead of  oc . For

1 *<collector\_pod\_name>*, specify the name of your Collector pod, for

example,  collector-vclg5 .

<a name="_page1_x39.00_y623.25"></a>Retrieving logs from a RHACS diagnostic bundle

You can also access Collector logs by downloading a diagnostic bundle from the Red Hat Advanced Cluster Security for Kubernetes (RHACS) user interface. Once you have downloaded the diagnostic bundle, you can inspect the logs for all the Collector pods. For more information, see G[enerating a diagnostic bundle.](https://docs.openshift.com/acs/4.4/configuration/generate-diagnostic-bundle.html)

<a name="_page2_x39.00_y56.25"></a>Analyzing the Collector pod status

Examining the pod’s most recent status is another easy way to determine the cause of a Collector crash. Failure messages are recorded to the most recent status and are accessible using the  kubectl describe pod or  oc describe pod command.

Procedure

- Describe the Collector pod:

$ oc describe pod -n stackrox *<collector\_pod\_name>* **(1)![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.008.png)**

If you use Kubernetes, enter  kubectl instead of  oc . For

1 *<collector\_pod\_name>*, specify the name of your Collector pod, for

example,  collector-vclg5 .

Example output

- ...![](Aspose.Words.78c64d02-6ccd-4471-9dee-27e2e298e964.009.png)

`    `Last State:     Terminated

`      `Reason:       Error

`      `Message:      No suitable kernel object downloaded **(1)**       Exit Code:    1

`      `Started:      Fri, 21 Oct 2022 11:50:56 +0100

`      `Finished:     Fri, 21 Oct 2022 11:51:25 +0100

- ...

In this example, you can see that Collector has failed to download a kernel 1

driver.
https://docs.openshift.com/acs/4.4/troubleshooting/retrieving-and-analyzing-the-collector-logs-and-pod-status.html 3/3


6/5/24, 2:28 PM Integrating with image registries | Integrating | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.001.png)![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.002.png)

Integrating with image registries

- [Automatic Configuration](#_page1_x39.00_y603.00)
- [Amazon ECR integrations](#_page2_x39.00_y137.25)
- [Manually configuring image registries](#_page2_x39.00_y497.25)
  - [Manually configuring OpenShift Container Platform registry](#_page2_x39.00_y568.50)
  - [Manually configuring Amazon Elastic Container Registry](#_page3_x39.00_y430.50)
  - [Manually configuring Google Container Registry](#_page9_x39.00_y510.00)
  - [Manually configuring Google Artifact Registry](#_page10_x39.00_y626.25)
  - [Manually configuring Microsoft Azure Container Registry](#_page11_x39.00_y538.50)
  - [Manually configuring JFrog Artifactory](#_page12_x39.00_y372.00)
  - [Manually configuring Quay Container Registry](#_page13_x39.00_y226.50)
- [Additional resources](#_page14_x39.00_y572.25)
  - [Manually configuring IBM Cloud Container Registry](#_page14_x39.00_y642.75)
  - [Manually configuring Red Hat Container Registry](#_page15_x39.00_y400.50)

Red Hat Advanced Cluster Security for Kubernetes (RHACS) integrates with a variety of image registries so that you can understand your images and apply security policies for image usage.

When you integrate with image registries, you can view important image details, such as image creation date and Dockerfile details (including image layers).

After you integrate RHACS with your registry, you can scan images, view image components, and apply security policies to images before or after deployment.

When you integrate with an image registry, RHACS does not scan all images in ![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.003.png)![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.004.png)your registry. RHACS only scans the images when you:

Use the images in deployments![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.005.png)

- Use the  roxctl CLI to check images

  Use a continuous integration (CI) system to enforce security policies

You can integrate RHACS with major image registries, including:

- [Amazon Elastic Container Registry (ECR)](https://aws.amazon.com/ecr/)
- [Docker Hub](https://hub.docker.com/)
- [Google Container Registry (GCR)](https://cloud.google.com/container-registry/)
- [Google Artifact Registry](https://cloud.google.com/artifact-registry/)
- [IBM Cloud Container Registry (ICR)](https://www.ibm.com/cloud/container-registry)
- [JFrog Artifactory](https://jfrog.com/artifactory/)
- [Microsoft Azure Container Registry (ACR)](https://azure.microsoft.com/en-au/services/container-registry/)
- [Red Hat Quay](https://quay.io/)
- [Red Hat container registries](https://access.redhat.com/RegistryAuthentication#red-hat-registries-1)
- [Sonatype Nexus](https://www.sonatype.com/nexus-repository-sonatype)
- Any other registry that uses the D[ocker Registry HTTP API](https://docs.docker.com/registry/spec/api/)

<a name="_page1_x39.00_y603.00"></a>Automatic Configuration

Red Hat Advanced Cluster Security for Kubernetes includes default integrations with standard registries, such as Docker Hub and others. It can also automatically configure integrations based on artifacts found in the monitored clusters, such as image pull secrets. Usually, you do not need to configure registry integrations manually.

https://docs.openshift.com/acs/4.4/integration/integrate-with-image-registries.html 2/16
6/5/24, 2:28 PM Integrating with image registries | Integrating | Red Hat Advanced Cluster Security for Kubernetes 4.4

- If you are using a GCR registry, Red Hat Advanced Cluster Security for ![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.006.png)![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.007.png)Kubernetes does not create a registry integration automatically.

<a name="_page2_x39.00_y137.25"></a>Amazon ECR integrations

For Amazon ECR integrations, Red Hat Advanced Cluster Security for Kubernetes automatically generates ECR registry integrations if the following conditions are met:

- The cloud provider for the cluster is AWS.
- The nodes in your cluster have an Instance Identity and Access Management (IAM) Role association and the Instance Metadata Service is available in the nodes. For example, when using Amazon Elastic Kubernetes Service (EKS) to manage your cluster, this role is known as the EKS Node IAM role.
- The Instance IAM role has IAM policies granting access to the ECR registries from which you are deploying.

If the listed conditions are met, Red Hat Advanced Cluster Security for Kubernetes monitors deployments that pull from ECR registries and automatically generates ECR integrations for them. You can edit these integrations after they are automatically generated.

<a name="_page2_x39.00_y497.25"></a>Manually configuring image registries

If you are using GCR, you must manually create image registry integrations.

<a name="_page2_x39.00_y568.50"></a>Manually configuring OpenShift Container Platform registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes with OpenShift Container Platform built-in container image registry.

Prerequisites

- You need a username and a password for authentication with the OpenShift Container Platform registry.

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Generic Docker Registry .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Endpoint : The address of the registry.
  - Username and Password .
- If you are not using a TLS certificate when connecting to the registry, select Disable TLS certificate validation (insecure) .
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page3_x39.00_y430.50"></a>Manually configuring Amazon Elastic Container Registry

You can use Red Hat Advanced Cluster Security for Kubernetes to create and modify Amazon Elastic Container Registry (ECR) integrations manually. If you are deploying from Amazon ECR, integrations for the Amazon ECR registries are usually automatically generated. However, you might want to create integrations on your own to scan images outside deployments. You can also modify the parameters of an automatically-generated integration. For example, you can change the authentication method used by an automatically-generated Amazon ECR integration to use AssumeRole authentication or other authorization models.

To erase changes you made to an automatically-generated ECR ![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.008.png)![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.009.png)integration, delete the integration, and Red Hat Advanced Cluster

- Security for Kubernetes creates a new integration for you with the automatically-generated parameters when you deploy images from

  Amazon ECR.

Prerequisites

- You must have an Amazon Identity and Access Management (IAM) access key ID and a secret access key. Alternatively, you can use a node-level IAM proxy such as kiam or  kube2iam.
- The access key must have read access to ECR. See Ho[w do I create an AWS access key? f](https://aws.amazon.com/premiumsupport/knowledge-center/create-access-key/)or more information.
- If you are running Red Hat Advanced Cluster Security for Kubernetes in Amazon Elastic Kubernetes Service (EKS) and want to integrate with an ECR from a separate Amazon account, you must first set a repository policy statement in your ECR. Follow the instructions at S[etting a repository policy statement and fo](https://docs.aws.amazon.com/AmazonECR/latest/userguide/set-repository-policy.html)r Actions , choose the following scopes of the Amazon ECR API operations:
  - ecr:BatchCheckLayerAvailability
  - ecr:BatchGetImage
  - ecr:DescribeImages
  - ecr:GetDownloadUrlForLayer
  - ecr:ListImages

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Amazon ECR.
- Click New integration , or click one of the automatically-generated integrations to open it, then click Edit .
- Enter or modify the details for the following fields:
  - Update stored credentials : Clear this box if you are modifying an integration without updating the credentials such as access keys and passwords.
  - Integration name : The name of the integration.
  - Registry ID: The ID of the registry.
  - Endpoint : The address of the registry. This value is required only if you are using a private virtual private cloud (VPC) endpoint for Amazon ECR. This field is not enabled when the AssumeRole option is selected.
  - Region : The region for the registry; for example,  us-west-1 .
- If you are using IAM, select Use Container IAM role . Otherwise, clear the Use Container IAM role box and enter the Access key ID and Secret access key.
- If you are using AssumeRole authentication, select Use AssumeRole and enter the details for the following fields:
  - AssumeRole ID: The ID of the role to assume.
  - AssumeRole External ID (optional): If you are using an exter[nal ID with AssumeRole,](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html) you can enter it here.
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

Using assumerole with Amazon ECR

You can use [AssumeRole t](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html)o grant access to AWS resources without manually configuring each user’s permissions. Instead, you can define a role with the desired permissions so that the user is granted access to assume that role.  AssumeRole enables you to grant, revoke, or otherwise generally manage more fine-grained permissions.

**Configuring AssumeRole with container IAM**

Before you can use AssumeRole with Red Hat Advanced Cluster Security for Kubernetes, you must first configure it.

Procedure

- Enable the IAM OIDC provider for your EKS cluster:

$ eksctl utils associate-iam-oidc-provider --cluster <cluster name> --approve![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.010.png)

- [Create an IAM role f](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html)or your EKS cluster.
- Associate the newly created role with a service account:

$ kubectl -n stackrox annotate sa central eks.amazonaws.com/role- arn=arn:aws:iam::67890:role/<role-name>![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.011.png)

- Restart Central to apply the changes.

$ kubectl -n stackrox delete pod -l app=central![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.012.png)

- Assign the role to a policy that allows the role to assume another role as required:

{![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.013.png)

`    `"Version": "2012-10-17",

`    `"Statement": [

`        `{

`            `"Sid": "VisualEditor0",

`            `"Effect": "Allow",

`            `"Action": "sts:AssumeRole",

`            `"Resource": "arn:aws:iam::<ecr- registry>:role/<assumerole-readonly>" **(1)**         }

`    `]

}

1 Replace  <assumerole-readonly> with the role you want to assume.

- Update the trust relationship for the role you want to assume:

{![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.014.png)

`  `"Version": "2012-10-17",

`  `"Statement": [

`    `{

`      `"Effect": "Allow",

`      `"Principal": {

`        `"AWS": [

`          `"arn:aws:iam::<ecr-registry>:role/<role-name>" **(1)**         ]

`      `},

`      `"Action": "sts:AssumeRole"

`    `}

`  `]

}

1 The  <role-name> should match with the new role you have created earlier.

**Configuring AssumeRole without container IAM**

To use AssumeRole without container IAM, you must use an access and a secret key to authenticate as an A[WS user with programmatic access.](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html)

Procedure

- Depending on whether the AssumeRole user is in the same account as the ECR registry or in a different account, you must either:
  - Create a new role with the desired permissions if the user for which you want to assume role is in the same account as the ECR registry.
- When creating the role, you can choose any trusted entity as required. However, you ![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.015.png)![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.016.png)must modify it after creation.
- Or, you must provide permissions to access the ECR registry and define its trust relationship if the user is in a different account than the ECR registry:

  {![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.017.png)

  `    `"Version": "2012-10-17",

  `    `"Statement": [

  `        `{

  `            `"Sid": "VisualEditor0",

  `            `"Effect": "Allow",

  `            `"Action": "sts:AssumeRole",

  `            `"Resource": "arn:aws:iam::<ecr- registry>:role/<assumerole-readonly>" **(1)**         }

  `    `]

  }

  1 Replace  <assumerole-readonly> with the role you want to assume.

- Configure the trust relationship of the role by including the user ARN under the Principal field:

{![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.018.png)

`  `"Version": "2012-10-17",   "Statement": [

`    `{

`      `"Effect": "Allow",       "Principal": {

`        `"AWS": [

`          `"arn:aws:iam::<ecr-registry>:user/<role-name>"         ]

`      `},

`      `"Action": "sts:AssumeRole"

`    `}

`  `]

}

**Configuring AssumeRole in RHACS**

After configuring AssumeRole in ECR, you can integrate Red Hat Advanced Cluster Security for Kubernetes with Amazon Elastic Container Registry (ECR) by using AssumeRole.

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Amazon ECR.
- Click New Integration .
- Enter the details for the following fields:
  - Integration Name : The name of the integration.
  - Registry ID: The ID of the registry.
  - Region : The region for the registry; for example,  us-west-1 .
- If you are using IAM, select Use container IAM role . Otherwise, clear the Use custom IAM role box and enter the Access key ID and Secret access key.
- If you are using AssumeRole, select Use AssumeRole and enter the details for the following fields:
  - AssumeRole ID: The ID of the role to assume.
  - AssumeRole External ID (optional): If you are using an exter[nal ID with AssumeRole,](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html) you can enter it here.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page9_x39.00_y510.00"></a>Manually configuring Google Container Registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes with Google Container Registry (GCR).

Prerequisites

- You need either a w[orkload identity or a](https://cloud.google.com/kubernetes-engine/docs/how-to/workload-identity) service account key for authentication.
- The associated service account must have access to the registry. See Confi[guring access control f](https://cloud.google.com/container-registry/docs/access-control)or information about granting users and other projects access to GCR.
- If you are using [GCR Container Analysis, y](https://cloud.google.com/container-registry/docs/container-analysis)ou must also grant the following roles to the service account:
  - Container Analysis Notes Viewer
  - Container Analysis Occurrences Viewer
  - Storage Object Viewer

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Google Container Registry .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Type : Select Registry .
  - Registry Endpoint : The address of the registry.
  - Project : The Google Cloud project name.
  - Use workload identity : Check to authenticate using a workload identity.
  - Service account key (JSON) : Your service account key for authentication.
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page10_x39.00_y626.25"></a>Manually configuring Google Artifact Registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes with Google Artifact Registry.

Prerequisites

- You need either a w[orkload identity or a](https://cloud.google.com/kubernetes-engine/docs/how-to/workload-identity) service account key for authentication.
- The associated service account must have the Artifact Registry Reader Identity and Access Management (IAM) role  roles/artifactregistry.reader .

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Google Artifact Registry .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Registry endpoint : The address of the registry.
  - Project : The Google Cloud project name.
  - Use workload identity : Check to authenticate using a workload identity.
  - Service account key (JSON) : Your service account key for authentication.
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page11_x39.00_y538.50"></a>Manually configuring Microsoft Azure Container Registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes with Microsoft Azure Container Registry.

Prerequisites

- You must have a username and a password for authentication.

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Microsoft Azure Container Registry .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Endpoint : The address of the registry.
  - Username and Password .
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page12_x39.00_y372.00"></a>Manually configuring JFrog Artifactory

You can integrate Red Hat Advanced Cluster Security for Kubernetes with JFrog Artifactory.

Prerequisites

- You must have a username and a password for authentication with JFrog Artifactory.

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select JFrog Artifactory .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Endpoint : The address of the registry.
  - Username and Password .
- If you are not using a TLS certificate when connecting to the registry, select Disable TLS certificate validation (insecure) .
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page13_x39.00_y226.50"></a>Manually configuring Quay Container Registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes (RHACS) with Quay Container Registry. You can integrate with Quay by using the following methods:

- Integrating with the Quay public repository (registry): This method does not require authentication.
- Integrating with a Quay private registry by using a robot account: This method requires that you create a robot account to use with Quay (recommended). See the [Quay documentation fo](https://access.redhat.com/documentation/en-us/red_hat_quay/3/html/use_red_hat_quay/use-quay-manage-repo#allow-robot-access-user-repo)r more information.
- Integrating with Quay to use the Quay scanner rather than the RHACS scanner: This method uses the API and requires an OAuth token for authentication. See "Integrating with Quay Container Registry to scan images" in the "Additional Resources" section.

Prerequisites

- For authentication with a Quay private registry, you need the credentials associated with a robot account or an OAuth token (deprecated).

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Red Hat Quay.io .
- Click New integration .
- Enter the Integration name.
- Enter the Endpoint , or the address of the registry.
  - If you are integrating with the Quay public repository, under Type , select Registry , and then go to the next step.
  - If you are integrating with a Quay private registry, under Type , select Registry and enter information in the following fields:
    - Robot username : If you are accessing the registry by using a Quay robot account, enter the user name in the format  *<namespace>+ <accountname>*.
    - Robot password : If you are accessing the registry by using a Quay robot account, enter the password for the robot account user name.
    - OAuth token : If you are accessing the registry by using an OAuth token (deprecated), enter it in this field.
- Optional: If you are not using a TLS certificate when connecting to the registry, select Disable TLS certificate validation (insecure) .
- Optional: To create the integration without testing, select Create integration without testing .
- Select Save .
- If you are editing a Quay integration but do not want to update your ![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.019.png)![](Aspose.Words.a9955b3e-2889-42fb-9737-0c3a4463f144.020.png)credentials, verify that Update stored credentials is not selected.

<a name="_page14_x39.00_y572.25"></a>Additional resources

- [Integrating with Quay Container Registry to scan images](https://docs.openshift.com/acs/4.4/integration/integrate-with-image-vulnerability-scanners.html#integrate-with-qcr-scanner_integrate-with-image-vulnerability-scanners)

<a name="_page14_x39.00_y642.75"></a>Manually configuring IBM Cloud Container Registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes with IBM Cloud Container Registry.

Prerequisites

- You must have an API key for authentication with the IBM Cloud Container Registry.

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select IBM Cloud Container Registry .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Endpoint : The address of the registry.
  - API key .
- Select Test to test that the integration with the selected registry is working.
- Select Save .

<a name="_page15_x39.00_y400.50"></a>Manually configuring Red Hat Container Registry

You can integrate Red Hat Advanced Cluster Security for Kubernetes with Red Hat Container Registry.

Prerequisites

- You must have a username and a password for authentication with the Red Hat Container Registry.

Procedure

- In the RHACS portal, go to Platform Configuration → Integrations .
- Under the Image Integrations section, select Red Hat Registry .
- Click New integration .
- Enter the details for the following fields:
  - Integration name : The name of the integration.
  - Endpoint : The address of the registry.
  - Username and Password .
- Select Create integration without testing to create the integration without testing the connection to the registry.
- Select Test to test that the integration with the selected registry is working.
- Select Save .
https://docs.openshift.com/acs/4.4/integration/integrate-with-image-registries.html 16/16

6/5/24, 2:26 PM Installing the roxctl CLI | roxctl CLI | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.001.png)![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.002.png)

Installing the roxctl CLI

- [Installing the roxctl CLI by downloading the binary](#_page0_x39.00_y411.00)
  - [Installing the roxctl CLI on Linux](#_page0_x39.00_y503.25)
  - [Installing the roxctl CLI on macOS](#_page1_x39.00_y394.50)
  - [Installing the roxctl CLI on Windows](#_page2_x39.00_y295.50)
- [Running the roxctl CLI from a container](#_page2_x39.00_y640.50)

roxctl is a command-line interface (CLI) for running commands on Red Hat Advanced Cluster Security for Kubernetes (RHACS). You can install the  roxctl CLI by downloading the binary or you can run the  roxctl CLI from a container image.

<a name="_page0_x39.00_y411.00"></a>Installing the roxctl CLI by downloading the binary

You can install the  roxctl CLI to interact with RHACS from a command-line interface. You can install  roxctl on Linux, Windows, or macOS.

<a name="_page0_x39.00_y503.25"></a>Installing the roxctl CLI on Linux

You can install the  roxctl CLI binary on Linux by using the following procedure.

- roxctl CLI for Linux is available for  amd64 ,  ppc64le , and  s390x ![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.003.png)![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.004.png)architectures.

Procedure

- Determine the  roxctl architecture for the target operating system:

$ arch="$(uname -m | sed "s/x86\_64//")"; arch="${arch:+-$arch}"![ref1]

- Download the  roxctl CLI:

$ curl -f -o roxctl "https://mirror.openshift.com/pub/rhacs/assets/4.4.2/bin/Linux/ro xctl${arch}"![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.006.png)

- Make the  roxctl binary executable:

$ chmod +x roxctl![ref2]

- Place the  roxctl binary in a directory that is on your  PATH: To check your  PATH, execute the following command:

$ echo $PATH![ref3]

Verification

- Verify the  roxctl version you have installed: $ roxctl version![ref2]

<a name="_page1_x39.00_y394.50"></a>Installing the roxctl CLI on macOS

You can install the  roxctl CLI binary on macOS by using the following procedure.

- ![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.009.png) roxctl CLI for macOS is available for the  amd64 architecture.![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.010.png)

Procedure

- Download the  roxctl CLI:

$ curl -f -O https://mirror.openshift.com/pub/rhacs/assets/4.4.2/bin/Darwin/ro xctl![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.011.png)

- Remove all extended attributes from the binary: $ xattr -c roxctl![ref1]
- Make the  roxctl binary executable:

$ chmod +x roxctl![ref3]

- Place the  roxctl binary in a directory that is on your  PATH: To check your  PATH, execute the following command:

$ echo $PATH![ref3]

Verification

- Verify the  roxctl version you have installed: $ roxctl version![ref3]

<a name="_page2_x39.00_y295.50"></a>Installing the roxctl CLI on Windows

You can install the  roxctl CLI binary on Windows by using the following procedure.

Z

roxctl CLI for Windows is available for the  amd64 architecture. ![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.012.png)![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.013.png)Procedure

- Download the  roxctl CLI:

$ curl -f -O https://mirror.openshift.com/pub/rhacs/assets/4.4.2/bin/Windows/r oxctl.exe![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.014.png)

Verification

- Verify the  roxctl version you have installed: $ roxctl version![ref3]

<a name="_page2_x39.00_y640.50"></a>Running the roxctl CLI from a container

The  roxctl client is the default entry point in the RHACS  roxctl image. To run the

roxctl client in a container image:

Prerequisites

- You must first generate an authentication token from the RHACS portal.

Procedure

- Log in to the  registry.redhat.io registry.

$ docker login registry.redhat.io![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.015.png)

- Pull the latest container image for the  roxctl CLI.

$ docker pull registry.redhat.io/advanced-cluster-security/rhacs- roxctl-rhel8:4.4.2![ref4]

After you install the CLI, you can run it by using the following command:

$ docker run -e ROX\_API\_TOKEN=$ROX\_API\_TOKEN \![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.017.png)

`  `-it registry.redhat.io/advanced-cluster-security/rhacs-roxctl- rhel8:4.4.2 \

`  `-e $ROX\_CENTRAL\_ADDRESS <command>

In Red Hat Advanced Cluster Security Cloud Service (RHACS Cloud Service),![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.018.png)![](Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.019.png) when using  roxctl commands that require the Central

- aIndsdtraenssc,euDsee ttahielsCseencttrioanl ionfs ttahnecReeaddHdaret sHsy barsi dd iCsplolauyde Cd oinn sthoele. For example, use  acs-ABCD12345.acs.rhcloud.com instead of  acs -

  data-ABCD12345.acs.rhcloud.com.

Verification

- Verify the  roxctl version you have installed.

$ docker run -it registry.redhat.io/advanced-cluster- security/rhacs-roxctl-rhel8:4.4.2 version![ref4]
https://docs.openshift.com/acs/4.4/cli/installing-the-roxctl-cli.html 4/4

[ref1]: Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.005.png
[ref2]: Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.007.png
[ref3]: Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.008.png
[ref4]: Aspose.Words.a9143ca0-2e3c-41be-974c-c297cb324b70.016.png

6/5/24, 2:27 PM High-level RHACS installation overview | Installing | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.001.png)![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.002.png)

High-level RHACS installation overview

- [General installation guidelines](#_page0_x39.00_y633.75)
- [Installation methods for different platforms](#_page1_x39.00_y96.00)
- [Installation methods for different architectures](#_page2_x39.00_y370.50)
- [Installation steps for RHACS on OpenShift Container Platform](#_page3_x39.00_y56.25)
  - [Installing RHACS on Red Hat OpenShift by using the RHACS Operator](#_page3_x39.00_y98.25)
  - [Installing RHACS on Red Hat OpenShift by using Helm charts](#_page4_x39.00_y56.25)
  - [Installing RHACS on Red Hat OpenShift by using the  roxctl CLI](#_page4_x39.00_y525.00)
- [Installation steps for RHACS on Kubernetes](#_page5_x39.00_y270.00)
  - [Installing RHACS on Kubernetes platforms by using Helm charts](#_page5_x39.00_y312.00)
  - [Installing RHACS on Kubernetes platforms by using the  roxctl CLI](#_page6_x39.00_y56.25)

Red Hat Advanced Cluster Security for Kubernetes (RHACS) provides security services for your self-managed Red Hat OpenShift Kubernetes systems or platforms such as OpenShift Container Platform, Amazon Elastic Kubernetes Service (Amazon EKS), Google Kubernetes Engine (Google GKE), and Microsoft Azure Kubernetes Service (Microsoft AKS).

For information about supported platforms and architecture, see the Red H[at Advanced Cluster Security for Kubernetes Support Matrix. For ](https://access.redhat.com/articles/7045053)life cycle support information for RHACS, see the R[ed Hat Advanced Cluster Security for Kubernetes Support Policy.](https://access.redhat.com/support/policy/updates/rhacs)

<a name="_page0_x39.00_y633.75"></a>General installation guidelines

To ensure the best installation experience, follow these guidelines:

- Understand the installation platforms and methods described in this module.
- Understand [Red Hat Advanced Cluster Security for Kubernetes architecture.](https://docs.openshift.com/acs/4.4/architecture/acs-architecture.html#acs-architecture_acs-architecture)
- Check the [default resource requirements.](https://docs.openshift.com/acs/4.4/installing/acs-default-requirements.html#acs-default-requirements)

<a name="_page1_x39.00_y96.00"></a>Installation methods for different platforms

You can perform different types of installations on different platforms.

Not all installation methods are supported for all platforms. See the![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.003.png)![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.004.png)

Z [Red Hat Advanced Cluster Security for Kubernetes Support Matrix for ](https://access.redhat.com/articles/7045053)more information.

*Table 1. Platforms and recommended installation methods*

Recommended ![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.005.png)![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.006.png)![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.007.png)![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.008.png)

Platform type Platform installation methods Installation steps

Managed service Red Hat OpenShift Operator In[stalling Central ](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)platform Dedicated (OSD) (recommended), Helm s[ervices for](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)

charts, or  roxctl CLI R[HACS on ](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)Azure Red Hat [1] [Red Hat ](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)OpenShift (ARO) [OpenShift](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)

[Installing Secured ](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-secured-cluster-ocp.html#install-secured-cluster-ocp)Red Hat OpenShift [Cluster services ](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-secured-cluster-ocp.html#install-secured-cluster-ocp)Service on AWS (ROSA) [for RHACS on](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-secured-cluster-ocp.html#install-secured-cluster-ocp)

[Red Hat](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-secured-cluster-ocp.html#install-secured-cluster-ocp)

Red Hat OpenShift on [OpenShift](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-secured-cluster-ocp.html#install-secured-cluster-ocp)

IBM Cloud

Amazon Elastic Helm charts I[nstalling Central ](https://docs.openshift.com/acs/4.4/installing/installing_other/install-central-other.html#install-central-other)Kubernetes Service (recommended), or se[rvices for ](https://docs.openshift.com/acs/4.4/installing/installing_other/install-central-other.html#install-central-other)(Amazon EKS) roxctl CLI [1] R[HACS on other](https://docs.openshift.com/acs/4.4/installing/installing_other/install-central-other.html#install-central-other)

[platforms](https://docs.openshift.com/acs/4.4/installing/installing_other/install-central-other.html#install-central-other)

Google Kubernetes I[nstalling Secured ](https://docs.openshift.com/acs/4.4/installing/installing_other/install-secured-cluster-other.html#install-secured-cluster-other)Engine (Google GKE) [Cluster services](https://docs.openshift.com/acs/4.4/installing/installing_other/install-secured-cluster-other.html#install-secured-cluster-other)

[for RHACS on ](https://docs.openshift.com/acs/4.4/installing/installing_other/install-secured-cluster-other.html#install-secured-cluster-other)Microsoft Azure [other platforms ](https://docs.openshift.com/acs/4.4/installing/installing_other/install-secured-cluster-other.html#install-secured-cluster-other)Kubernetes Service

(Microsoft AKS)



<table><tr><th colspan="1" valign="top">Platform type</th><th colspan="1" valign="top">Platform</th><th colspan="1">Recommended installation methods</th><th colspan="1" valign="top">Installation steps</th></tr>
<tr><td colspan="1" rowspan="2" valign="top">Self-managed platform</td><td colspan="1" valign="top">Red Hat OpenShift Container Platform (OCP)</td><td colspan="1" rowspan="2" valign="top"><p>Operator (recommended), Helm charts, or  roxctl CLI</p><p>[1]</p></td><td colspan="1" rowspan="2" valign="top"><p>- [Installing Central services for RHACS on](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)</p><p>&emsp;[Red Hat OpenShift](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-central-ocp.html#install-central-ocp)</p><p>- [Installing Secured Cluster services for RHACS on Red Hat OpenShift](https://docs.openshift.com/acs/4.4/installing/installing_ocp/install-secured-cluster-ocp.html#install-secured-cluster-ocp)</p></td></tr>
<tr><td colspan="1" valign="top">Red Hat OpenShift Kubernetes Engine (OKE)</td></tr>
</table>

- Do not use the  roxctl installation method unless you have specific requirements for following this installation method.

<a name="_page2_x39.00_y370.50"></a>Installation methods for different architectures

Red Hat Advanced Cluster Security for Kubernetes (RHACS) supports the following architectures. For information on supported platforms and architecture, see the Red [Hat Advanced Cluster Security for Kubernetes Support Matrix. Add](https://access.redhat.com/articles/7045053)itionally, the following table gives information about installation methods available for each architecture.

*Table 2. Architectures and supported installation methods for each architecture*

Supported architectures Supported installation methods![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.009.png)![](Aspose.Words.c6372781-d320-482e-a89d-90abc4d7a7f7.010.png)

AMD64 Operator (preferred), Helm charts, or  roxctl CLI

(not recommended)

ppc64le (IBM Power) Operator s390x (IBM Z and IBM® LinuxONE)

<a name="_page3_x39.00_y56.25"></a>Installation steps for RHACS on OpenShift Container Platform

<a name="_page3_x39.00_y98.25"></a>Installing RHACS on Red Hat OpenShift by using the RHACS Operator

- On the Red Hat OpenShift cluster, install the RHACS Operator into the  rhacs - operator project, or namespace.
- On the Red Hat OpenShift cluster that will contain Central, called the central cluster, use the RHACS Operator to install Central services into the  stackrox project. One central cluster can secure multiple clusters.
- Log in to the RHACS web console from the central cluster, and then create an init bundle and download it. The init bundle is then installed on the cluster that you want to secure, called the secured cluster.
- For the secured cluster:
  - Install the RHACS Operator into the  rhacs-operator namespace.
  - On the secured cluster, apply the init bundle that you created in RHACS by performing one of these steps:
    - Use the OpenShift Container Platform web console to import the YAML file of the init bundle that you created. Make sure you are in the stackrox namespace.
    - In the terminal window, run the  oc create -f <init\_bundle>.yaml

      -n <stackrox> command, specifying the path to the downloaded

      YAML file of the init bundle.

- On the secured cluster, use the RHACS Operator to install Secured Cluster services into the  stackrox namespace. When creating these services, be sure to enter the address and port number of Central in the Central Endpoint field so that the secured cluster can communicate with Central.

<a name="_page4_x39.00_y56.25"></a>Installing RHACS on Red Hat OpenShift by using Helm charts

- Add the RHACS Helm charts repository.
- Install the  central-services Helm chart on the Red Hat OpenShift cluster that will contain Central, called the central cluster.
- Log in to the RHACS web console on the Central cluster and create an init bundle.
- For each cluster that you want to secure, log in to the secured cluster and perform the following steps:
  - Apply the init bundle you created with RHACS. To apply the init bundle on the secured cluster, perform one of these steps:
    - Use the OpenShift Container Platform web console to import the YAML file of the init bundle that you created. Make sure you are in the stackrox namespace.
    - In the terminal window, run the  oc create -f <init\_bundle>.yaml -n <stackrox> command, specifying the path to the downloaded YAML file of the init bundle.
  - Install the  secured-cluster-services Helm chart on the secured cluster, specifying the path to the init bundle that you created.

<a name="_page4_x39.00_y525.00"></a>Installing RHACS on Red Hat OpenShift by using the roxctl CLI

This installation method is also called the *manifest installation method*.

- Install the  roxctl CLI.
- On the Red Hat OpenShift cluster that will contain Central, perform these steps:
  - In the terminal window, run the interactive install command by using the roxctl CLI.
  - Run the setup shell script.
  - In the terminal window, create the Central resources by using the  oc create command.
- Perform one of the following actions:
  - In the RHACS web console, create and download the sensor YAML file and keys.
  - On the secured cluster, use the  roxctl sensor generate openshift command.
- On the secured cluster, run the sensor installation script.

<a name="_page5_x39.00_y270.00"></a>Installation steps for RHACS on Kubernetes

<a name="_page5_x39.00_y312.00"></a>Installing RHACS on Kubernetes platforms by using Helm charts

- Add the RHACS Helm charts repository.
- Install the  central-services Helm chart on the cluster that will contain Central, called the Central cluster.
- Log in to the RHACS web console from the Central cluster and create an init bundle that you will install on the cluster that you want to secure, called the secured cluster.
- For each secured cluster:
  - Apply the init bundle you created with RHACS. Log in to the secured cluster and run the  kubectl create -f <init\_bundle>.yaml -n <stackrox> command, specifying the path to the downloaded YAML file of the init bundle.
  - Install the  secured-cluster-services Helm chart on the secured cluster, specifying the path to the init bundle that you created earlier.

<a name="_page6_x39.00_y56.25"></a>Installing RHACS on Kubernetes platforms by using the roxctl CLI

This installation method is also called the *manifest installation method*.

- Install the  roxctl CLI.
- On the Kubernetes cluster that will contain Central, perform these steps:
  - In the terminal window, run the interactive install command by using the roxctl CLI.
  - Run the setup shell script.
  - In the terminal window, create the Central resources by using the  kubectl create command.
- Perform one of the following actions:
  - In the RHACS web console, create and download the sensor YAML file and keys.
  - On the cluster that you want to secure, called the secured cluster, use the roxctl sensor generate openshift command.
- On the secured cluster, run the sensor installation script.
https://docs.openshift.com/acs/4.4/installing/acs-high-level-overview.html 7/7


6/5/24, 2:28 PM Backing up Red Hat Advanced Cluster Security for Kubernetes | Backup and restore | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.001.png)![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.002.png)

Backing up Red Hat Advanced Cluster Security for Kubernetes

- [Backing up Central database by using the roxctl CLI](#_page1_x39.00_y312.00)
  - [On-demand backups by using an API token](#_page2_x39.00_y56.25)
  - [On-demand backups by using the administrator password](#_page2_x39.00_y534.75)
- [Backing up Central deployment](#_page3_x39.00_y260.25)
  - [Backing up deployment using the RHACS Operator](#_page3_x39.00_y488.25)
  - [Backing up deployment using Helm](#_page4_x39.00_y237.00)

You can perform data backups for Red Hat Advanced Cluster Security for Kubernetes and use these for data restoration in case of an infrastructure disaster or corrupt data.

You can configure automatic backups for the Central database by integrating with [Amazon S3 ](https://docs.openshift.com/acs/4.4/integration/integrate-with-amazon-s3.html#perform-on-demand-backups-amazon-s3_integrate-with-amazon-s3)or [Google Cloud Storage. Yo](https://docs.openshift.com/acs/4.4/integration/integrate-with-google-cloud-storage.html#perform-on-demand-backups-google-cloud-storage_integrate-with-google-cloud-storage)u can perform on-demand backups of the Central database by using the  roxctl CLI. You can also back up your Central deployment using RHACS Operator or Helm Chart installation methods.

Depending on your requirements, you can create two types of backups:

- A backup of the Central database: It includes RHACS configurations, resources, events, and certificates. In an unforeseen incident, such as database failure or data corruption, you can use the backup to recover and restore the Central database to its earlier functional state. Doing this ensures the availability and integrity of essential data, allowing you to continue normal operations without significant disruptions or loss of critical information.
- A backup of all custom deployment configurations: If you installed RHACS by using Helm charts or the RHACS Operator, you can back up settings, parameters, and customizations specific to your installation. When the RHACS installation gets accidentally deleted, or you need to migrate it to another cluster or namespace, having a backup of the deployment configurations enables a seamless recovery process. In addition, by restoring the custom settings from the backup, you can efficiently reinstate your Central installation’s unique requirements and configurations, ensuring consistent and exact deployment of the system.

Because backup files include secrets and certificates, you must securely store the backup files.

<a name="_page1_x39.00_y312.00"></a>Backing up Central database by using the roxctl CLI

Backing up the Central database is critical to ensure data integrity and system reliability. Regular backups of the database, containing necessary configurations, resources, events, and certificates, protect against database failures, corruption, and accidental data loss.

You can use the  roxctl CLI to take the backups by using the  backup command. You require an API token or your administrator password to run this command.

Red Hat supports backups for the Central database through ![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.003.png)![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.004.png)integration with [Amazon S3 or](https://docs.openshift.com/acs/4.4/integration/integrate-with-amazon-s3.html#perform-on-demand-backups-amazon-s3_integrate-with-amazon-s3) G[oogle Cloud Storage.](https://docs.openshift.com/acs/4.4/integration/integrate-with-google-cloud-storage.html#perform-on-demand-backups-google-cloud-storage_integrate-with-google-cloud-storage)

- Backing up to Amazon S3 API-compatible storage might work. However, Red Hat does not test and support Amazon S3 API- compatible storage for backing up RHACS. For example, see RHA[CS backup on MinIO.](https://access.redhat.com/solutions/7021082)

<a name="_page2_x39.00_y56.25"></a>On-demand backups by using an API token

You can back up the entire database of RHACS by using an API token. Prerequisites

- You have an API token with the  Admin role.
- You have installed the  roxctl CLI.

Procedure

- Set the  ROX\_API\_TOKEN and the  ROX\_ENDPOINT environment variables by running the following commands:

$ export ROX\_API\_TOKEN=<api\_token>![ref1]

$ export ROX\_ENDPOINT=<address>:<port\_number>![ref2]

- Initiate a backup for Central by running the following command:

$ roxctl central backup **(1)![ref1]**

1 You can use the  --output option to specify the backup file location.

By default, the  roxctl CLI saves the backup file in the directory where you run the command.

Additional resources

- [System roles](https://docs.openshift.com/acs/4.4/operating/manage-user-access/manage-role-based-access-control-3630.html#rbac-system-roles-3630_manage-role-based-access-control)

<a name="_page2_x39.00_y534.75"></a>On-demand backups by using the administrator password

You can back up the entire database of RHACS by using your administrator password.

Prerequisites

- You have the administrator password.
- You have installed the  roxctl CLI.

Procedure

- Set the  ROX\_ENDPOINT environment variable by running the following command:

$ export ROX\_ENDPOINT=<address>:<port\_number>![ref2]

- Initiate a backup for Central by running the following command:

$ roxctl -p <admin\_password> central backup **(1)![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.007.png)**

1 For  <admin\_password> , specify the administrator password.

By default, the  roxctl CLI saves the backup file in the directory in which you run the command. You can use the  --output option to specify the backup file location.

<a name="_page3_x39.00_y260.25"></a>Backing up Central deployment

You can back up the deployment of a Central instance. This can be useful if you want to migrate central to another namespace or cluster by using the same configuration values.

Red Hat does not support backing up deployment configurations by![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.008.png)![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.009.png)

- using the  roxctl CLI. You can use the  oc or  kubectl CLI to back up manifests related to your Central instance and restore the configuration.

<a name="_page3_x39.00_y488.25"></a>Backing up deployment using the RHACS Operator

When you use the RHACS Operator to instal RHACS, OpenShift Container Platform stores all the custom configuration for your Central deployment within the Central custom resource. You can backup the Central custom resource, the  central-tls

secret, and the administrator password. The  central-tls secret includes the certificates for authenticating with Secured clusters and signing API tokens.

Procedure

- Run the following command to save the Central custom resource in a YAML file:

$ oc get central -n \_<central-namespace>\_ \_<central-name>\_ -o yaml > central-cr.yaml![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.010.png)

- Run the following command to save  central-tls in a JSON file:

$ oc get secret -n \_<central-namespace>\_ central-tls -o json | jq 'del(.metadata.ownerReferences)' > central-tls.json![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.011.png)

- Run the following command to the administrator password in a JSON file:

$ oc get secret -n \_<central-namespace>\_ central-htpasswd -o json | jq 'del(.metadata.ownerReferences)' > central-htpasswd.json![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.012.png)

<a name="_page4_x39.00_y237.00"></a>Backing up deployment using Helm

When you use the Helm chart to install RHACS, you store all the custom configuration for your Central deployment within the custom values that you apply to the Helm chart.

You can back up the custom values and save it in a YAML file.

Procedure

- Run the following command to back up custom Helm chart values in a YAML file:

$ helm get values --all -n \_<central-namespace>\_ \_<central-helm- release>\_ -o yaml > central-values-backup.yaml![](Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.013.png)
https://docs.openshift.com/acs/4.4/backup\_and\_restore/backing-up-acs.html 5/5

[ref1]: Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.005.png
[ref2]: Aspose.Words.e4afd1e9-54fa-410f-aee0-9356a890a1d6.006.png

6/5/24, 2:28 PM Backing up Central database by using the roxctl CLI | Troubleshooting Central | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.001.png)![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.002.png)

Backing up Central database by using the roxctl CLI

- [On-demand backups by using an API token](#_page0_x39.00_y569.25)
- [On-demand backups by using the administrator password](#_page1_x39.00_y375.00)

Central stores information about the following:

- Activity observed in your clusters
- Information retrieved from integrated image registries or Scanners
- Red Hat Advanced Cluster Security for Kubernetes (RHACS) configuration

Backing up the Central database is critical to ensure data integrity and system reliability. Regular backups of the database, which contain the necessary configurations, resources, events, and certificates, protect against database failures, corruption, and accidental data loss.

You can use the  roxctl CLI to back up and restore the Central database by using the

backup command. This command requires an API token or your administrator password.

<a name="_page0_x39.00_y569.25"></a>On-demand backups by using an API token

You can back up the entire database of RHACS by using an API token. Prerequisites

- You have an API token with the  Admin role.
- You have installed the  roxctl CLI.

Procedure

- Set the  ROX\_API\_TOKEN and the  ROX\_ENDPOINT environment variables by running the following commands:

$ export ROX\_API\_TOKEN=<api\_token>![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.003.png)

$ export ROX\_ENDPOINT=<address>:<port\_number>![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.004.png)

- Initiate a backup for Central by running the following command:

$ roxctl central backup **(1)![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.005.png)**

1 You can use the  --output option to specify the backup file location.

By default, the  roxctl CLI saves the backup file in the directory where you run the command.

Additional resources

- [System roles](https://docs.openshift.com/acs/4.4/operating/manage-user-access/manage-role-based-access-control-3630.html#rbac-system-roles-3630_manage-role-based-access-control)

<a name="_page1_x39.00_y375.00"></a>On-demand backups by using the administrator password

You can back up the entire database of RHACS by using your administrator password.

Prerequisites

- You have the administrator password.
- You have installed the  roxctl CLI.

Procedure

- Set the  ROX\_ENDPOINT environment variable by running the following command: $ export ROX\_ENDPOINT=<address>:<port\_number>![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.006.png)
- Initiate a backup for Central by running the following command:

  $ roxctl -p <admin\_password> central backup **(1) ![](Aspose.Words.f244cc58-441d-49e7-8e85-873a46cb9811.007.png)**1 For  <admin\_password> , specify the administrator password.

  By default, the  roxctl CLI saves the backup file in the directory in which you run the command. You can use the  --output option to specify the backup file location.
https://docs.openshift.com/acs/4.4/troubleshooting\_central/backing-up-central-database-by-using-the-roxctl-cli.html 2/2


6/5/24, 2:27 PM Adding custom certificates | Configuring | Red Hat Advanced Cluster Security for Kubernetes 4.4

` `![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.001.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.002.png)

Adding custom certificates

- [Adding a custom security certificate](#_page0_x39.00_y497.25)
  - [Prerequisites for adding custom certificates](#_page0_x39.00_y589.50)
  - [Adding a custom certificate during a new installation](#_page1_x39.00_y444.00)
  - [Adding a custom certificate for an existing instance](#_page3_x39.00_y195.75)
  - [Updating the custom certificate for an existing instance](#_page5_x39.00_y139.50)
- [Configuring Sensor to trust custom certificates](#_page6_x39.00_y109.50)
  - [Downloading a Sensor bundle](#_page6_x39.00_y315.75)
  - [Configuring Sensor to trust custom certificates when deploying a new Sensor](#_page7_x39.00_y318.75)
  - [Configuring an existing Sensor to trust custom certificates](#_page8_x39.00_y354.75)

Learn how to use a custom TLS certificate with Red Hat Advanced Cluster Security for Kubernetes. After you set up a certificate, users and API clients do not have to bypass the certificate security warnings when connecting to Central.

<a name="_page0_x39.00_y497.25"></a>Adding a custom security certificate

You can apply a security certificate during the installation or on an existing Red Hat Advanced Cluster Security for Kubernetes deployment.

<a name="_page0_x39.00_y589.50"></a>Prerequisites for adding custom certificates

Prerequisites

- You must already have PEM-encoded private key and certificate files.
- The certificate file should begin and end with human-readable blocks. For example:

-----BEGIN CERTIFICATE----- MIICLDCCAdKgAwIBAgIBADAKBggqhkjOPQQDAjB9MQswCQYDVQQGEwJCRTEPMA0G ...![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.003.png)

l4wOuDwKQa+upc8GftXE2C//4mKANBC6It01gUaTIpo=

-----END CERTIFICATE-----

- The certificate file can contain either a single (leaf) certificate, or a certificate chain.

If the certificate is not directly signed by a trusted root, you ![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.004.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.005.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.006.png)must provide the full certificate chain, including any intermediate certificates.

q All certificates in the chain must be in order so that the leaf certificate is the first and the root certificate is the last in the chain.

- If you are using a custom certificate that is not globally trusted, you must also configure the Sensor to trust your custom certificate.

<a name="_page1_x39.00_y444.00"></a>Adding a custom certificate during a new installation

Procedure

- If you are installing Red Hat Advanced Cluster Security for Kubernetes using the Operator:
  - Create a  central-default-tls-cert secret that contains the appropriate TLS certificates in the namespace where the Central service will be installed by entering the following command:

    oc -n <namespace> create secret tls central-default-tls-cert --cert <tls-cert.pem> --key <tls-key.pem>![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.007.png)

- If you are installing Red Hat Advanced Cluster Security for Kubernetes using Helm:
  - Add your custom certificate and its key in the  values-private.yaml file:

    central:![ref1]

- Configure a default TLS certificate (public cert + 

private key) for central

`  `defaultTLS:

`    `cert: |

`      `-----BEGIN CERTIFICATE-----

EXAMPLE!MIIMIICLDCCAdKgAwIBAgIBADAKBggqhkjOPQQDAjB9MQswCQYDVQ QGEwJCRTEPMA0G

...

`      `-----END CERTIFICATE-----

`    `key: |

`      `-----BEGIN EC PRIVATE KEY-----

`      `EXAMPLE!MHcl4wOuDwKQa+upc8GftXE2C//4mKANBC6It01gUaTIpo=       ...

`      `-----END EC PRIVATE KEY-----

- Provide the configuration file during the installation:

  $ helm install -n stackrox --create-namespace stackrox- central-services rhacs/central-services -f values- private.yaml![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.009.png)

- If you are installing Red Hat Advanced Cluster Security for Kubernetes using the roxctl CLI, provide the certificate and key files when you run the installer:
  - For the non-interactive installer, use the  --default-tls-cert and  - - default-tls-key options:

    $ roxctl central generate --default-tls-cert "cert.pem" -- default-tls-key "key.pem"![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.010.png)

- For the interactive installer, provide the certificate and key files when you enter answers for the prompts:

  ...![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.011.png)

  Enter PEM cert bundle file (optional): <cert.pem> Enter PEM private key file (optional): <key.pem> Enter administrator password (default: autogenerated): Enter orchestrator (k8s, openshift): openshift

  ...

<a name="_page3_x39.00_y195.75"></a>Adding a custom certificate for an existing instance

Procedure

- If you have installed Red Hat Advanced Cluster Security for Kubernetes using the Operator:
  - Create a  central-default-tls-cert secret that contains the appropriate TLS certificates in the namespace where the Central service is installed by entering the following command:

    oc -n <namespace> create secret tls central-default-tls-cert --cert <tls-cert.pem> --key <tls-key.pem>![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.012.png)

- If you have installed Red Hat Advanced Cluster Security for Kubernetes using Helm:
  - Add your custom certificate and its key in the  values-private.yaml file:

    central:![ref1]

- Configure a default TLS certificate (public cert + 

private key) for central

`  `defaultTLS:

`    `cert: |

`      `-----BEGIN CERTIFICATE-----

EXAMPLE!MIIMIICLDCCAdKgAwIBAgIBADAKBggqhkjOPQQDAjB9MQswCQYDVQ QGEwJCRTEPMA0G

...

`      `-----END CERTIFICATE-----

`    `key: |

`      `-----BEGIN EC PRIVATE KEY-----

`      `EXAMPLE!MHcl4wOuDwKQa+upc8GftXE2C//4mKANBC6It01gUaTIpo=       ...

`      `-----END EC PRIVATE KEY-----

- Use the  helm upgrade command and provide the updated configuration file:

  $ helm upgrade -n stackrox --create-namespace stackrox- central-services \![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.013.png)

  ` `rhacs/central-services --reuse-values \**(1)**

  ` `-f values-private.yaml

  You must use this parameter because the  values-private.yaml file 1

does not contain all of the required configuration values.

- If you have installed Red Hat Advanced Cluster Security for Kubernetes using the roxctl CLI:
  - Create and apply a TLS secret from the PEM-encoded key and certificate files:

    $ oc -n stackrox create secret tls central-default-tls-cert \   --cert <server\_cert.pem> \![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.014.png)

    `  `--key <server\_key.pem> \

    `  `--dry-run -o yaml | oc apply -f -

    After you run this command, Central automatically applies the new key and certificate without requiring the pod to be restarted. It might take up to a minute to propagate the changes.

<a name="_page5_x39.00_y139.50"></a>Updating the custom certificate for an existing instance

If you use a custom certificate for Central, you can update the certificate by performing the following procedure.

Procedure

- Delete the existing custom certificate’s secret:

$ oc delete secret central-default-tls-cert![ref2]

- Create a new secret:

$ oc -n stackrox create secret tls central-default-tls-cert \   --cert <server\_cert.pem> \![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.016.png)

`  `--key <server\_key.pem> \

`  `--dry-run -o yaml | oc apply -f -

- Restart the Central container.

Restarting the Central container

You can restart the Central container by killing the Central container or by deleting the Central pod.

Procedure

- Run the following command to kill the Central container:

You must wait for at least 1 minute, until OpenShift Container![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.017.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.018.png)

- Platform propagates your changes and restarts the Central container.

$ oc -n stackrox exec deploy/central -c central -- kill 1![ref2]

- Or, run the following command to delete the Central pod:

$ oc -n stackrox delete pod -lapp=central![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.019.png)

<a name="_page6_x39.00_y109.50"></a>Configuring Sensor to trust custom certificates

If you are using a custom certificate that is not trusted globally, you must configure the Sensor to trust your custom certificate. Otherwise, you might get errors. The specific type of error may vary based on your setup and the certificate you use. Usually, it is an

x509 validation related error.

- You do not need to configure the Sensor to trust your custom ![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.020.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.021.png)certificate if you are using a globally trusted certificate.

<a name="_page6_x39.00_y315.75"></a>Downloading a Sensor bundle

The Sensor bundle includes the necessary configuration files and scripts to install Sensor. You can download the Sensor bundle from the RHACS portal.

Procedure

- In the RHACS portal, go to Platform Configuration → Clusters .
- Click New Cluster and specify a name for the cluster.
- If you are deploying the Sensor in the same cluster, accept the default values for all the fields. Otherwise, if you are deploying into a different cluster, replace the address  central.stackrox.svc:443 with a load balancer, node port, or other address (including the port number) that is accessible from the other cluster in which you are planning to install.

If you are using a non-gRPC capable load balancer, such as HAProxy, AWS Application Load ![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.022.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.023.png)Balancer (ALB), or AWS Elastic Load Balancing (ELB) use the WebSocket Secure ( wss )

- protocol. To use  wss :

Prefix the address with  wss:// , and![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.024.png)

Add the port number after the address, for example, wss://stackrox-central.example.com:443 .

- Click Next to continue.
- Click Download YAML File and Keys .

<a name="_page7_x39.00_y318.75"></a>Configuring Sensor to trust custom certificates when deploying a new Sensor

Prerequisites

- You have downloaded the Sensor bundle.

Procedure

- If you are using the  sensor.sh script:
  - Unzip the Sensor bundle:

    $ unzip -d sensor sensor-<cluster\_name>.zip![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.025.png)

- Run the  sensor.sh script:

  $ ./sensor/sensor.sh![ref3]

  The certificates are automatically applied when you run the sensor ( ./sensor/sensor.sh ) script. You can also place additional custom certificates in the  sensor/additional-cas/ directory before you run the

  sensor.sh script.

- If you are not using the  sensor.sh script:
  - Unzip the Sensor bundle:

    $ unzip -d sensor sensor-<cluster\_name>.zip![ref3]

- Run the following command to create the secret:

  $ ./sensor/ca-setup-sensor.sh -d sensor/additional-cas/ **(1) ![ref4]**1 Use the  -d option to specify a directory containing custom certificates.

If you get the "secret already exists" error message, re-run ![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.028.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.029.png)the script with the  -u option:

Z ![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.030.png)

$ ./sensor/ca-setup-sensor.sh -d sensor/additional-cas/ -u

- Continue Sensor deployment by using the YAML files.

<a name="_page8_x39.00_y354.75"></a>Configuring an existing Sensor to trust custom certificates

Prerequisites

- You have downloaded the Sensor bundle.

Procedure

- Unzip the Sensor bundle:

$ unzip -d sensor sensor-<cluster\_name>.zip![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.031.png)

- Run the following command to create the secret:

  $ ./sensor/ca-setup-sensor.sh -d sensor/additional-cas/ **(1) ![ref2]**1 Use the  -d option to specify a directory containing custom certificates.

If you get the "secret already exists" error message, re-run the![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.032.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.033.png)

script with the  -u option:

Z ![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.034.png)

$ ./sensor/ca-setup-sensor.sh -d sensor/additional- cas/ -u

- Continue Sensor deployment by using the YAML files.

If you added the certificates to an existing sensor, you must restart the Sensor container.

Restarting the Sensor container

You can restart the Sensor container either by killing the container or by deleting the Sensor pod.

Procedure

- Run the following command to kill the Sensor container:

You must wait for at least 1 minute, until OpenShift Container![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.035.png)![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.036.png)

- Platform or Kubernetes propagates your changes and restarts the Sensor container.
- On OpenShift Container Platform:

  $ oc -n stackrox deploy/sensor -c sensor -- kill 1![ref3]

- On Kubernetes:

  $ kubectl -n stackrox deploy/sensor -c sensor -- kill 1![ref4]

- Or, run the following command to delete the Sensor pod:
  - On OpenShift Container Platform:

    $ oc -n stackrox delete pod -lapp=sensor![](Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.037.png)

- On Kubernetes:

  $ kubectl -n stackrox delete pod -lapp=sensor![ref3]
https://docs.openshift.com/acs/4.4/configuration/add-custom-certificates.html 9/9

[ref1]: Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.008.png
[ref2]: Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.015.png
[ref3]: Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.026.png
[ref4]: Aspose.Words.d5e938ba-530a-4681-a02c-a3fdd3f51eaf.027.png
