<p>Packages:</p>
<ul>
<li>
<a href="#alerts.newrelic.io%2fv1alpha1">alerts.newrelic.io/v1alpha1</a>
</li>
<li>
<a href="#dashboards.newrelic.io%2fv1alpha1">dashboards.newrelic.io/v1alpha1</a>
</li>
</ul>
<h2 id="alerts.newrelic.io/v1alpha1">alerts.newrelic.io/v1alpha1</h2>
<p>
<p>Package v1alpha1 contains API Schema definitions for the io v1alpha1 API group</p>
</p>
Resource Types:
<ul></ul>
<h3 id="alerts.newrelic.io/v1alpha1.AlertPolicy">AlertPolicy
</h3>
<p>
<p>AlertPolicy is the Schema for the newrelicalertpolicies API</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metadata</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicySpec">
AlertPolicySpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the alert policy that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>incident_preference</code></br>
<em>
string
</em>
</td>
<td>
<p>The incident preference defines when incident should be created. <br />
Can be one of: <br />
- <code>per_policy</code> <br />
- <code>per_condition</code> <br />
- <code>per_condition_and_target</code> </p>
</td>
</tr>
<tr>
<td>
<code>apmConditions</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.ApmCondition">
[]ApmCondition
</a>
</em>
</td>
<td>
<em>optional</em>
<p>A list of APM alert conditions to attach to the policy</p>
</td>
</tr>
<tr>
<td>
<code>nrqlConditions</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.NrqlCondition">
[]NrqlCondition
</a>
</em>
</td>
<td>
<em>optional</em>
<p>A list of NRQL alert conditions to attach to the policy</p>
</td>
</tr>
<tr>
<td>
<code>infraConditions</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.InfraCondition">
[]InfraCondition
</a>
</em>
</td>
<td>
<em>optional</em>
<p>A list of Infrastructure alert conditions to attach to the policy</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicyStatus">
AlertPolicyStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.AlertPolicySpec">AlertPolicySpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicy">AlertPolicy</a>)
</p>
<p>
<p>AlertPolicySpec defines the desired state of AlertPolicy.
Detailed parameter description can be found on the official <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/rest-api-calls-new-relic-alerts#policies">New Relic documentation</a></p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the alert policy that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>incident_preference</code></br>
<em>
string
</em>
</td>
<td>
<p>The incident preference defines when incident should be created. <br />
Can be one of: <br />
- <code>per_policy</code> <br />
- <code>per_condition</code> <br />
- <code>per_condition_and_target</code> </p>
</td>
</tr>
<tr>
<td>
<code>apmConditions</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.ApmCondition">
[]ApmCondition
</a>
</em>
</td>
<td>
<em>optional</em>
<p>A list of APM alert conditions to attach to the policy</p>
</td>
</tr>
<tr>
<td>
<code>nrqlConditions</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.NrqlCondition">
[]NrqlCondition
</a>
</em>
</td>
<td>
<em>optional</em>
<p>A list of NRQL alert conditions to attach to the policy</p>
</td>
</tr>
<tr>
<td>
<code>infraConditions</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.InfraCondition">
[]InfraCondition
</a>
</em>
</td>
<td>
<em>optional</em>
<p>A list of Infrastructure alert conditions to attach to the policy</p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.AlertPolicyStatus">AlertPolicyStatus
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicy">AlertPolicy</a>)
</p>
<p>
<p>AlertPolicySpec defines the observed state of AlertPolicy</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>status</code></br>
<em>
string
</em>
</td>
<td>
<p>The value will be set to <code>created</code> once the policy has been created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>reason</code></br>
<em>
string
</em>
</td>
<td>
<p>When a policy fails to be created, the value will be set to the error message received from New Relic</p>
</td>
</tr>
<tr>
<td>
<code>newrelicPolicyId</code></br>
<em>
int64
</em>
</td>
<td>
<p>The policy id in New Relic</p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.ApmCondition">ApmCondition
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicySpec">AlertPolicySpec</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the alert condition that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>type</code></br>
<em>
string
</em>
</td>
<td>
<p>The type of the metric to monitor. Should be one of: <br />
- <code>apm_app_metric</code> <br />
- <code>apm_kt_metric</code> <br />
- <code>apm_jvm_metric</code> <br />
- <code>browser_metric</code> <br />
- <code>mobile_metric</code> <br />
Please refer to the Alerts conditions section in the <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#type">New Relic documentation</a> for more details</p>
</td>
</tr>
<tr>
<td>
<code>enabled</code></br>
<em>
bool
</em>
</td>
<td>
<em>optional</em>
<p><em>default: true</em></p>
</td>
</tr>
<tr>
<td>
<code>conditionScope</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
<tr>
<td>
<code>entities</code></br>
<em>
[]string
</em>
</td>
<td>
<p>A list of application names from APM to monitor</p>
</td>
</tr>
<tr>
<td>
<code>violationCloseTimer</code></br>
<em>
int
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
<tr>
<td>
<code>runbookUrl</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
<tr>
<td>
<code>metric</code></br>
<em>
string
</em>
</td>
<td>
<p>The APM metric to monitor. Different metrics can be applied depending on the condition type. <br />
An example of a valid (type, metric) combination is (apm_app_metric, apdex). <br />
Please refer to the Alerts conditions section in the <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#metric">New Relic documentation</a> for more details</p>
</td>
</tr>
<tr>
<td>
<code>alertThreshold</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.Threshold">
Threshold
</a>
</em>
</td>
<td>
<p>Once the alertThreshold is breached, a critical incident will be generated</p>
</td>
</tr>
<tr>
<td>
<code>warningThreshold</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.Threshold">
Threshold
</a>
</em>
</td>
<td>
<em>optional</em>
<p>Once the warningThreshold is breached, a warning will be generated</p>
</td>
</tr>
<tr>
<td>
<code>userDefined</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.UserDefined">
UserDefined
</a>
</em>
</td>
<td>
<em>optional</em>
<p>Used for tracking a user defined custom metric <br />
For more information, please refer to the <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#user_defined_metric">New Relic documentation</a></p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.ChannelFactory">ChannelFactory
</h3>
<p>
</p>
<h3 id="alerts.newrelic.io/v1alpha1.EmailNotificationChannel">EmailNotificationChannel
</h3>
<p>
<p>EmailNotificationChannel is the Schema for the EmailNotificationChannels API</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metadata</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.EmailNotificationChannelSpec">
EmailNotificationChannelSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the notification channel created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>recipients</code></br>
<em>
string
</em>
</td>
<td>
<p>A comma-separated value of emails</p>
</td>
</tr>
<tr>
<td>
<code>includeJsonAttachment</code></br>
<em>
bool
</em>
</td>
<td>
<em>optional</em>
<p><em>default: false</em></p>
<p>Include JSON attachment with the notification</p>
</td>
</tr>
<tr>
<td>
<code>policySelector</code></br>
<em>
k8s.io/apimachinery/pkg/labels.Set
</em>
</td>
<td>
<p>A label selector defining the alert policies covered by the notification channel</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.NotificationChannelStatus">
NotificationChannelStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.EmailNotificationChannelSpec">EmailNotificationChannelSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.EmailNotificationChannel">EmailNotificationChannel</a>)
</p>
<p>
<p>EmailNotificationChannelSpec defines the desired state of EmailNotificationChannel</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the notification channel created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>recipients</code></br>
<em>
string
</em>
</td>
<td>
<p>A comma-separated value of emails</p>
</td>
</tr>
<tr>
<td>
<code>includeJsonAttachment</code></br>
<em>
bool
</em>
</td>
<td>
<em>optional</em>
<p><em>default: false</em></p>
<p>Include JSON attachment with the notification</p>
</td>
</tr>
<tr>
<td>
<code>policySelector</code></br>
<em>
k8s.io/apimachinery/pkg/labels.Set
</em>
</td>
<td>
<p>A label selector defining the alert policies covered by the notification channel</p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.InfraCondition">InfraCondition
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicySpec">AlertPolicySpec</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the infra condition that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>comparison</code></br>
<em>
string
</em>
</td>
<td>
<p>Available options are: <br />
- <code>above</code> <br />
- <code>below</code> <br />
- <code>equal</code> </p>
</td>
</tr>
<tr>
<td>
<code>alertThreshold</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.InfraThreshold">
InfraThreshold
</a>
</em>
</td>
<td>
<p>Once the alertThreshold is breached, a critical incident will be generated</p>
</td>
</tr>
<tr>
<td>
<code>warningThreshold</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.InfraThreshold">
InfraThreshold
</a>
</em>
</td>
<td>
<em>optional</em>
<p>Once the warningThreshold is breached, a warning will be generated</p>
</td>
</tr>
<tr>
<td>
<code>enabled</code></br>
<em>
bool
</em>
</td>
<td>
<em>optional</em>
<p><em>default: true</em></p>
</td>
</tr>
<tr>
<td>
<code>eventType</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
<p>Leave this parameter empty when creating conditions based on data from an integration provider
For more information, please refer to the <code>event_type</code> field in the official <a href="https://docs.newrelic.com/docs/infrastructure/new-relic-infrastructure/infrastructure-alert-conditions/rest-api-calls-new-relic-infrastructure-alerts#definitions">New Relic documentation</a></p>
</td>
</tr>
<tr>
<td>
<code>integrationProvider</code></br>
<em>
string
</em>
</td>
<td>
<p>When setting up alerts on integrations, specify the corresponding integration provider. <br />
Examples can include SqsQueue, Kubernetes, RdsDbInstance etc. <br />
For more information, please refer to the <code>integration_provider</code> field in the official <a href="https://docs.newrelic.com/docs/infrastructure/new-relic-infrastructure/infrastructure-alert-conditions/rest-api-calls-new-relic-infrastructure-alerts#definitions">New Relic documentation</a></p>
</td>
</tr>
<tr>
<td>
<code>runbookUrl</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
<tr>
<td>
<code>selectValue</code></br>
<em>
string
</em>
</td>
<td>
<p>The attribute name from the Event sample or Integration provider which identifies the metric to be tracked.
Examples for Sqs include <code>provider.approximateAgeOfOldestMessage.Average</code> and <code>provider.numberOfEmptyReceives.Average</code>.
For more information, please refer to the <code>select_value</code> field in the official <a href="https://docs.newrelic.com/docs/infrastructure/new-relic-infrastructure/infrastructure-alert-conditions/rest-api-calls-new-relic-infrastructure-alerts#definitions">New Relic documentation</a></p>
</td>
</tr>
<tr>
<td>
<code>violationCloseTimer</code></br>
<em>
int
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
<tr>
<td>
<code>whereClause</code></br>
<em>
string
</em>
</td>
<td>
<p>An expression used for filtering data from the IntegrationProvider</p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.InfraThreshold">InfraThreshold
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.InfraCondition">InfraCondition</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>timeFunction</code></br>
<em>
string
</em>
</td>
<td>
<p>Defines when the threshold should be considered as breached. <br />
Available options are: <br />
- <code>all</code> - all data points are in violation within the given period <br />
- <code>any</code> - at least one data point is in violation within the given period </p>
</td>
</tr>
<tr>
<td>
<code>value</code></br>
<em>
int
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>durationMinutes</code></br>
<em>
int
</em>
</td>
<td>
<p>For how long the violation should be active before an incident is triggered </p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.NotificationChannel">NotificationChannel
</h3>
<p>
</p>
<h3 id="alerts.newrelic.io/v1alpha1.NotificationChannelStatus">NotificationChannelStatus
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.EmailNotificationChannel">EmailNotificationChannel</a>, 
<a href="#alerts.newrelic.io/v1alpha1.SlackNotificationChannel">SlackNotificationChannel</a>)
</p>
<p>
<p>NotificationChannelStatus defines the observed state of NotificationChannel</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>status</code></br>
<em>
string
</em>
</td>
<td>
<p>The value will be set to <code>created</code> once the policy has been created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>reason</code></br>
<em>
string
</em>
</td>
<td>
<p>When a policy fails to be created, the value will be set to the error message received from New Relic</p>
</td>
</tr>
<tr>
<td>
<code>newrelicChannelId</code></br>
<em>
int64
</em>
</td>
<td>
<p>The channel id in New Relic</p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.NrqlCondition">NrqlCondition
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.AlertPolicySpec">AlertPolicySpec</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the nrql policy that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>enabled</code></br>
<em>
bool
</em>
</td>
<td>
<em>optional</em>
<p><em>default: true</em></p>
</td>
</tr>
<tr>
<td>
<code>query</code></br>
<em>
string
</em>
</td>
<td>
<p>The NRQL query associated with the condition</p>
</td>
</tr>
<tr>
<td>
<code>sinceMinutes</code></br>
<em>
int
</em>
</td>
<td>
<p>Defines the <code>SINCE</code> clause in the NRQL query</p>
</td>
</tr>
<tr>
<td>
<code>valueFunction</code></br>
<em>
string
</em>
</td>
<td>
<p>Available options are: <br />
- <code>single_value</code> <br />
- <code>sum</code> <br />
For more information, please refer to the official <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#value_function">New Relic documentation</a></p>
</td>
</tr>
<tr>
<td>
<code>alertThreshold</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.Threshold">
Threshold
</a>
</em>
</td>
<td>
<p>Once the alertThreshold is breached, a critical incident will be generated</p>
</td>
</tr>
<tr>
<td>
<code>warningThreshold</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.Threshold">
Threshold
</a>
</em>
</td>
<td>
<em>optional</em>
<p>Once the warningThreshold is breached, a warning will be generated</p>
</td>
</tr>
<tr>
<td>
<code>runbookUrl</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.SlackNotificationChannel">SlackNotificationChannel
</h3>
<p>
<p>NotificationChannel is the Schema for the slacknotificationchannels API</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metadata</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.SlackNotificationChannelSpec">
SlackNotificationChannelSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the notification channel created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>url</code></br>
<em>
string
</em>
</td>
<td>
<p>The Slack webhook URL</p>
</td>
</tr>
<tr>
<td>
<code>channel</code></br>
<em>
string
</em>
</td>
<td>
<p>Name of the Slack channel. Should start with <code>#</code></p>
</td>
</tr>
<tr>
<td>
<code>policySelector</code></br>
<em>
k8s.io/apimachinery/pkg/labels.Set
</em>
</td>
<td>
<p>A label selector defining the alert policies covered by the notification channel</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code></br>
<em>
<a href="#alerts.newrelic.io/v1alpha1.NotificationChannelStatus">
NotificationChannelStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.SlackNotificationChannelSpec">SlackNotificationChannelSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.SlackNotificationChannel">SlackNotificationChannel</a>)
</p>
<p>
<p>SlackNotificationChannelSpec defines the desired state of NotificationChannel</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the notification channel created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>url</code></br>
<em>
string
</em>
</td>
<td>
<p>The Slack webhook URL</p>
</td>
</tr>
<tr>
<td>
<code>channel</code></br>
<em>
string
</em>
</td>
<td>
<p>Name of the Slack channel. Should start with <code>#</code></p>
</td>
</tr>
<tr>
<td>
<code>policySelector</code></br>
<em>
k8s.io/apimachinery/pkg/labels.Set
</em>
</td>
<td>
<p>A label selector defining the alert policies covered by the notification channel</p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.Threshold">Threshold
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.ApmCondition">ApmCondition</a>, 
<a href="#alerts.newrelic.io/v1alpha1.NrqlCondition">NrqlCondition</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>timeFunction</code></br>
<em>
string
</em>
</td>
<td>
<p>Defines when the threshold should be considered as breached. <br />
Available options are: <br />
* all - all data points are in violation within the given period <br />
* any - at least one data point is in violation within the given period <br />
For more information, please refer to the official <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#terms_time_function">New Relic documentation</a></p>
</td>
</tr>
<tr>
<td>
<code>operator</code></br>
<em>
string
</em>
</td>
<td>
<p>Available options are: <br />
- <code>above</code> <br />
- <code>below</code> <br />
- <code>equal</code> </p>
</td>
</tr>
<tr>
<td>
<code>value</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>durationMinutes</code></br>
<em>
int
</em>
</td>
<td>
<p>For how long the violation should be active before an incident is triggered <br />
For more information, please refer to the official <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#terms_duration_minutes">New Relic documentation</a></p>
</td>
</tr>
</tbody>
</table>
<h3 id="alerts.newrelic.io/v1alpha1.UserDefined">UserDefined
</h3>
<p>
(<em>Appears on:</em>
<a href="#alerts.newrelic.io/v1alpha1.ApmCondition">ApmCondition</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metric</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the user defined custom metric</p>
</td>
</tr>
<tr>
<td>
<code>value_function</code></br>
<em>
string
</em>
</td>
<td>
<p>Available options are: <br />
- <code>average</code> <br />
- <code>min</code> <br />
- <code>max</code> <br />
- <code>total</code> <br />
- <code>sample_size</code> <br />
For more information, please refer to the official <a href="https://docs.newrelic.com/docs/alerts/rest-api-alerts/new-relic-alerts-rest-api/alerts-conditions-api-field-names#user_defined_value_function">New Relic documentation</a></p>
</td>
</tr>
</tbody>
</table>
<hr/>
<h2 id="dashboards.newrelic.io/v1alpha1">dashboards.newrelic.io/v1alpha1</h2>
<p>
<p>Package v1alpha1 contains API Schema definitions for the dashboards v1alpha1 API group</p>
</p>
Resource Types:
<ul></ul>
<h3 id="dashboards.newrelic.io/v1alpha1.Apm">Apm
</h3>
<p>
(<em>Appears on:</em>
<a href="#dashboards.newrelic.io/v1alpha1.Data">Data</a>)
</p>
<p>
<p>Apm is the set of metric parameters used for defining the data to plot in the widget</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>sinceSeconds</code></br>
<em>
int
</em>
</td>
<td>
<p>The time frame in seconds</p>
</td>
</tr>
<tr>
<td>
<code>entities</code></br>
<em>
[]string
</em>
</td>
<td>
<p>A list of application names for which to get the metric</p>
</td>
</tr>
<tr>
<td>
<code>metrics</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.Metric">
[]Metric
</a>
</em>
</td>
<td>
<p>A list of metrics to use</p>
</td>
</tr>
<tr>
<td>
<code>facet</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
<tr>
<td>
<code>order_by</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
</td>
</tr>
</tbody>
</table>
<h3 id="dashboards.newrelic.io/v1alpha1.Dashboard">Dashboard
</h3>
<p>
<p>DashboardBody is the Schema for the dashboards API</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metadata</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.DashboardSpec">
DashboardSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>title</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the dashboard that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>widgets</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.Widget">
[]Widget
</a>
</em>
</td>
<td>
<p>A list of widgets to add to the dashboard</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.DashboardStatus">
DashboardStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="dashboards.newrelic.io/v1alpha1.DashboardSpec">DashboardSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#dashboards.newrelic.io/v1alpha1.Dashboard">Dashboard</a>)
</p>
<p>
<p>DashboardSpec defines the desired state of DashboardBody</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>title</code></br>
<em>
string
</em>
</td>
<td>
<p>The name of the dashboard that will be created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>widgets</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.Widget">
[]Widget
</a>
</em>
</td>
<td>
<p>A list of widgets to add to the dashboard</p>
</td>
</tr>
</tbody>
</table>
<h3 id="dashboards.newrelic.io/v1alpha1.DashboardStatus">DashboardStatus
</h3>
<p>
(<em>Appears on:</em>
<a href="#dashboards.newrelic.io/v1alpha1.Dashboard">Dashboard</a>)
</p>
<p>
<p>DashboardStatus defines the observed state of DashboardBody</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>status</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>reason</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>newrelicDashboardId</code></br>
<em>
int64
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="dashboards.newrelic.io/v1alpha1.Data">Data
</h3>
<p>
(<em>Appears on:</em>
<a href="#dashboards.newrelic.io/v1alpha1.Widget">Widget</a>)
</p>
<p>
<p>Data represents the data to plot inside the widget. <br />
Either Nrql or ApmMetric should be specified, but not both. <br />
<br />
Leave both fields empty if you want to plot the application breakdown data, <br />
also present in the main widget that comes with the default application dashboard. <br />
For more information refer to the official <a href="https://docs.newrelic.com/docs/insights/insights-api/manage-dashboards/insights-dashboard-api#dashboard-data">New Relic documentation</a></p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>nrql</code></br>
<em>
string
</em>
</td>
<td>
<em>optional</em>
<p>The NRQL query used which defines the data to plot in the widget</p>
</td>
</tr>
<tr>
<td>
<code>apm</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.Apm">
Apm
</a>
</em>
</td>
<td>
<em>optional</em>
<p>The APM metric parameters which defines the data to plot in the widget. <br />
When using an APM metric for the data, visualization should be set to either <code>metric_line_chart</code> or <code>application_breakdown</code>. </p>
</td>
</tr>
</tbody>
</table>
<h3 id="dashboards.newrelic.io/v1alpha1.Metric">Metric
</h3>
<p>
(<em>Appears on:</em>
<a href="#dashboards.newrelic.io/v1alpha1.Apm">Apm</a>)
</p>
<p>
<p>Metric is the name of the metric as shown in Data Explorer</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>Name of the metric</p>
</td>
</tr>
<tr>
<td>
<code>values</code></br>
<em>
[]string
</em>
</td>
<td>
<p>List of metric values to plot. The available values will depend on the metric you choose. <br />
Check the Data Explorer in New Relic to find out which values are available for which metrics.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="dashboards.newrelic.io/v1alpha1.Widget">Widget
</h3>
<p>
(<em>Appears on:</em>
<a href="#dashboards.newrelic.io/v1alpha1.DashboardSpec">DashboardSpec</a>)
</p>
<p>
<p>Widget defines the widget parameters <br />
For more details, refer to the official <a href="https://docs.newrelic.com/docs/insights/insights-api/manage-dashboards/insights-dashboard-api#widget-data">New Relic documentation</a></p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>title</code></br>
<em>
string
</em>
</td>
<td>
<p>The title of the widget created in New Relic</p>
</td>
</tr>
<tr>
<td>
<code>visualization</code></br>
<em>
string
</em>
</td>
<td>
<p>Visualization type to use for the widget. <br />
Available options are: <br />
- <code>application_breakdown</code> <br />
- <code>attribute_sheet</code> <br />
- <code>background_breakdown</code> <br />
- <code>billboard</code> <br />
- <code>billboard_comparison</code> <br />
- <code>comparison_line_chart</code> <br />
- <code>event_table</code> <br />
- <code>facet_bar_chart</code> <br />
- <code>facet_pie_chart</code> <br />
- <code>facet_table</code> <br />
- <code>faceted_area_chart</code> <br />
- <code>faceted_line_chart</code> <br />
- <code>funnel</code> <br />
- <code>gauge</code> <br />
- <code>heatmap</code> <br />
- <code>histogram</code> <br />
- <code>json</code> <br />
- <code>line_chart</code> <br />
- <code>list</code> <br />
- <code>metric_line_chart</code> (used for apm metrics) </p>
</td>
</tr>
<tr>
<td>
<code>data</code></br>
<em>
<a href="#dashboards.newrelic.io/v1alpha1.Data">
Data
</a>
</em>
</td>
<td>
<p>The data to plot on the widget</p>
</td>
</tr>
<tr>
<td>
<code>layout</code></br>
<em>
github.com/fpetkovski/newrelic-alert-manager/pkg/dashboards/domain/widget.Layout
</em>
</td>
<td>
<p>Defines the layout of the widget within the dashboard</p>
</td>
</tr>
</tbody>
</table>
<hr/>
<p><em>
Generated with <code>gen-crd-api-reference-docs</code>
on git commit <code>5d91f19</code>.
</em></p>