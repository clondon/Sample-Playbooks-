# Access Revocation Playbook

## Overview
This playbook provides procedures for revoking user access across systems when an employee leaves the organization or when access needs to be removed for security reasons.

## Prerequisites
- IT administrator access to identity management systems
- List of systems and services requiring access revocation
- Human Resources notification or security incident documentation
- Access to audit logs

## Scope
- **Covers**: Account deactivation, credential revocation, access removal across all systems
- **Does not cover**: Data transfer or handoff procedures (covered in offboarding playbook)

## Roles and Responsibilities
- **IT Administrator**: Executes technical access revocation steps
- **Security Team**: Verifies complete access removal and monitors for suspicious activity
- **HR Representative**: Provides authorization and employee information
- **Manager**: Confirms completion and data handoff needs

## Procedure

### Step 1: Gather Information
Collect all necessary information about the user and access to be revoked.

**Action items:**
1. Obtain employee ID, username, and email address
2. Review user's group memberships and roles
3. Identify all systems and services the user has access to
4. Determine the effective date/time of access revocation
5. Understand the reason for revocation (termination, security incident, role change)
6. Note any special considerations (ongoing projects, credentials shared with others)

**Expected outcome:**
- Complete list of user's access points
- Clear timeline for revocation
- Special requirements documented

### Step 2: Disable Primary Accounts
Disable the user's main authentication mechanisms immediately.

**Action items:**
1. Disable Active Directory/LDAP account
2. Disable SSO/SAML access
3. Disable VPN access
4. Disable email account (or convert to shared mailbox if needed)
5. Disable multi-factor authentication (MFA) devices
6. Force logout from all active sessions

**Expected outcome:**
- Primary authentication disabled
- User cannot access corporate systems
- Active sessions terminated

### Step 3: Revoke System-Specific Access
Remove access from individual systems and applications.

**Action items:**
1. Remove from cloud platform accounts (AWS, Azure, GCP)
2. Revoke database access
3. Remove from code repositories (GitHub, GitLab, etc.)
4. Deactivate SaaS application accounts (Salesforce, JIRA, etc.)
5. Remove from communication platforms (Slack, Teams, etc.)
6. Revoke API keys and service account access
7. Remove from shared resources (network drives, SharePoint, etc.)

**Expected outcome:**
- All system-specific access removed
- User cannot access any corporate resources

### Step 4: Revoke Physical Access
Disable physical access to facilities and resources.

**Action items:**
1. Deactivate building access badges/cards
2. Notify security desk of revocation
3. Request return of company equipment (laptop, phone, tokens)
4. Update physical access logs
5. Remove from visitor management systems

**Expected outcome:**
- Physical access revoked
- Equipment return process initiated
- Security team notified

### Step 5: Rotate Shared Credentials
Change any passwords or credentials the user had access to.

**Action items:**
1. Identify all shared accounts or credentials the user had access to
2. Rotate passwords for shared accounts
3. Regenerate SSH keys if applicable
4. Rotate API keys used by user
5. Update credential documentation
6. Notify teams of credential changes

**Expected outcome:**
- All potentially compromised credentials rotated
- Teams notified of changes

### Step 6: Monitor and Verify
Ensure complete access revocation and monitor for any unauthorized attempts.

**Action items:**
1. Verify account shows as disabled in all systems
2. Check for any remaining active sessions
3. Review audit logs for any access attempts
4. Set up monitoring alerts for attempted access using revoked credentials
5. Confirm with system owners that access is revoked
6. Document completion time for each system

**Expected outcome:**
- Complete access revocation verified
- Monitoring in place for unauthorized attempts
- Documentation complete

## Verification
Confirm all access has been properly revoked:
1. Attempt login with user credentials (should fail)
2. Verify user does not appear in any active user lists
3. Check all group memberships are removed
4. Confirm no active sessions in audit logs
5. Validate physical access card is deactivated
6. Test that user cannot access email or VPN

## Rollback Procedure
If access was revoked in error:
1. Immediately notify IT security leadership
2. Re-enable primary accounts (AD/LDAP, SSO)
3. Restore group memberships from backup/documentation
4. Re-enable system-specific access
5. Reactivate physical access
6. Notify the user of the error and resolution
7. Document the incident for process improvement

## Post-Execution
- Complete access revocation checklist in HR system
- Document any challenges or delays encountered
- Update access revocation procedures if gaps identified
- Store revocation documentation per retention policy
- Schedule follow-up verification check (7 days post-revocation)
- Conduct team debrief if this was an emergency revocation

## Related Resources
- [Employee Offboarding Checklist]
- [System Access Inventory]
- [Credential Management Policy]
- [Security Incident Response Playbook]

## Changelog
| Date | Author | Changes |
|------|--------|---------|
| 2025-10-21 | System | Initial creation |
