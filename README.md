Remove a Stale User Account

Scenario
To maintain identity hygiene and enforce lifecycle governance, a user account that is no longer in use—jacob.choi@company.com
—must be removed from the Microsoft Entra tenant. This process includes disabling the account, verifying no active dependencies, and then permanently deleting the user. This reflects responsible identity deprovisioning and prevents the accumulation of stale objects that could be misused.

Step-by-Step Action Flow (Simulated)

Navigate to Microsoft Entra Admin Center → Users

Locate jacob.choi@company.com

Confirm user is inactive or no longer needed

Click Block sign-in → Confirm

Check group memberships and directory role assignments

Remove user from any security or role-assignable groups

Remove directory roles, if present

Click Delete user → Confirm deletion

Verify deletion by searching directory

Review audit logs to confirm user removal event

Entra Control Stack Mapping
Layer 1 – Authority Definition

✅ Touched
Action requires either User Administrator or Privileged Role Administrator rights. Logs reflect execution context for accountability.

Layer 2 – Scope Boundaries

✅ Relevant
While the user was directory-wide, cleanup actions reinforce containment and show deliberate boundary enforcement.

Layer 3 – Test Identity Validation

✅ Post-action validation
Confirm no authentication attempts or group inheritance remains post-removal. Validate group and role integrity.

Layer 4 – External Entry Controls

❌ Not affected
This user is internal. No cross-tenant implications are involved.

Layer 5 – Privilege Channels

✅ Engaged if the user had roles
If jacob.choi had privileged roles, this removal closes an unnecessary privilege path.

Layer 6 – Device Trust Enforcement

❌ Not affected
This process does not involve device trust posture or compliance status.

Layer 7 – Continuous Verification

✅ Follow-up
Ensure periodic identity review policies exist to flag stale accounts before long periods of dormancy. Recommend integration with access reviews or automated lifecycle policies.

Observations and Follow-Up

Removal was clean, with group memberships and roles revoked prior to deletion.

Audit logs confirm the action with traceable context.

Identity lifecycle policies should incorporate stale account checks to reduce manual oversight.

Suggest regular review cadence for stale accounts across departments.

Entra Control Stack: Micro-Project Series (Progress Tracker)
Project	Title	Status
1	Add a New Guest User	✅ Complete
2	Change a Global Administrator to a Privileged Role Administrator	✅ Complete
3	Assign User Administrator Role at AU Scope	✅ Complete
4	Remove a Stale User Account	✅ Complete
5	Create a Group and Assign Role	⬜ Upcoming
