# Installation

## Requirements

- Zabbix 7.0 server
- Zabbix server or proxy with network access to the card
- Delta InsightPower G3 Mini SNMP Card
- SNMPv2c enabled with a read-only community
- UDP/161 allowed between the monitoring component and the card

## Import

1. Open **Data collection → Templates**.
2. Select **Import**.
3. Choose one language:
   - `templates/template_delta_insightpower_g3_en.yaml`
   - `templates/template_delta_insightpower_g3_pt_BR.yaml`
4. Keep all import options enabled and complete the import.

The templates have different internal names and UUIDs, so both languages may be imported into the same Zabbix installation.

## Host configuration

1. Create a host with a descriptive name.
2. Add an **SNMP** interface with the card IP and UDP port 161.
3. Select SNMPv2 and enter the read-only community.
4. Select the Zabbix proxy when the UPS is reached through a remote site.
5. Link the imported template.
6. Check **Monitoring → Latest data** after a few polling intervals.

## Suggested security controls

- Use a unique read-only community.
- Permit UDP/161 only from the Zabbix server or proxy.
- Do not store the community in exported files or Git.
- Prefer a dedicated management VLAN.
