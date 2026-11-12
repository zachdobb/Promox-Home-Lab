## Rocky Linux Active Directory Lab Screenshots

### 1. Rocky Linux Network Configuration

Verified the Rocky Linux network configuration, including the VM IP address, DNS server, and hostname.

![Rocky Linux IP Address](../screenshots/09-rocky-ip-address.png)

![Rocky Linux DNS Configuration](../screenshots/10-rocky-dns-config.png)

![Rocky Linux Hostname](../screenshots/11-rocky-hostname.png)

### 2. Active Directory Domain Discovery

Verified that Rocky Linux could discover the `ad.homelab.test` Active Directory domain using `realm discover`.

![Rocky Linux Realm Discovery](../screenshots/12-rocky-realm-discovery.png)

### 3. Rocky Linux Domain Join

Confirmed that Rocky Linux was successfully joined to the Active Directory domain.

The `realm list` output showed:

`configured: kerberos-member`

![Rocky Linux Domain Join](../screenshots/13-rocky-domain-joined.png)

### 4. Active Directory User Verification

Verified that the Active Directory user `zdobbins@ad.homelab.test` was recognized by Rocky Linux and that domain group memberships were available.

![Rocky Linux Active Directory User](../screenshots/14-rocky-ad-user.png)

### 5. Active Directory Login Test

Successfully authenticated to Rocky Linux using the Active Directory account.

This confirmed that Active Directory authentication was working between Windows Server and Rocky Linux.

![Rocky Linux Active Directory Login](../screenshots/15-rocky-ad-login.png)
