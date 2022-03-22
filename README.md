# Repository for Mach ICO Contest

Have you ever heard about Policy as  Code? I'm sure you have.
Policy as Code lets you treat a policy like an application, leveraging version control, pull review, and automating tests.

Intersight integrates today with HashiCorp Terraform but lacks the integration with the robust Policy as Code solution offered by HashiCorp with Sentinel.
Sentinel is an embedded policy-as-code framework integrated with the HashiCorp Enterprise products such as Terraform Cloud. It enables fine-grained, logic-based policy decisions and can be extended to use information from external sources.

But what can you do with Sentinel? You can write a policy that prevents the destruction of your resources in your production environment. Or allowing only some particular provider to use by your plan. Or limit the type of EC2 instances you can create. Or ... okay, okay, you got it.

> **Note:**  The repo focus is on the support of Policy Set, as the usage of a single Policy is deprecated in Terraform Cloud. Policy sets are groups of policies that are applied together to related workspaces. Notice also Sentinel policies are a paid feature available as part of the Team & Governance upgrade package from HashiCorp.

Current use cases are highlighted below. These use cases can be implemented as ICO Workflow and rely on custom tasks:
 - Create a Policy Set and attach it to a workspace(s)
 - Update a given Policy Set
 - Detach a workspace(s) from a Policy Set

The above workflow relies on the below custom task:
 - Create a Policy Set
 - Delete a Policy Set
 - Update a Policy Set
 - Attach a Policy Set to a workspaces
 - Detach a Policy Set from a workspaces
