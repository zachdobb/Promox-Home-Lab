## Rocky Linux Active Directory Integration

I integrated a Rocky Linux 9 virtual machine into my existing Windows Server Active Directory environment. This allowed Active Directory users and groups to be recognized and authenticated on Linux.

### 1. Rocky Linux Network Configuration

The Rocky Linux VM was configured with a static IPv4 address.

- Rocky Linux IP: `192.168.1.220`
- Domain Controller/DNS: `192.168.1.83`
- Interface: `ens18`

![Rocky Linux IP](screenshots/09-rocky-ip-address.png)

### 2. DNS Configuration

Rocky Linux was configured to use the Windows Server domain controller as its DNS server so that Active Directory records could be resolved.

![Rocky Linux DNS](screenshots/10-rocky-dns-config.png)

### 3. Linux Hostname Configuration

The Rocky Linux hostname was configured as:

`rocky-linux.ad.homelab.test`

![Rocky Linux Hostname](screenshots/11-rocky-hostname.png)

### 4. Active Directory Discovery

The `realm discover` command confirmed that Rocky Linux could locate the `ad.homelab.test` Active Directory domain.

![Active Directory Discovery](screenshots/12-rocky-realm-discovery.png)

### 5. Rocky Linux Joined to Active Directory

Rocky Linux was successfully joined to the domain using `realmd`, Kerberos, and SSSD.

The `realm list` command confirmed the system was configured as a Kerberos domain member.

![Rocky Linux Domain Join](screenshots/13-rocky-domain-joined.png)

### 6. Active Directory User Verification

The Active Directory account `zdobbins@ad.homelab.test` was successfully recognized by Rocky Linux along with its domain group memberships.

![Active Directory User](screenshots/14-rocky-ad-user.png)

### 7. Active Directory Login Test

The Active Directory user successfully authenticated to Rocky Linux, demonstrating centralized authentication between Windows Active Directory and Linux.

![Active Directory Login](screenshots/15-rocky-ad-login.png)

### Skills Demonstrated

- Linux administration
- Active Directory integration
- DNS configuration and troubleshooting
- Kerberos authentication
- SSSD configuration
- Linux networking
- Cross-platform identity management
