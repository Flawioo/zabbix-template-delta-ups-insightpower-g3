# Zabbix Template for Delta UPS — InsightPower G3 Mini SNMP Card

Community Zabbix 7.0 template for monitoring Delta UPS devices equipped with the **InsightPower G3 Mini SNMP Card** over SNMPv2c.

[Português](#português) | [English](#english)

## English

### Features

- UPS and SNMP card identification
- Input voltage and frequency
- Output voltage, frequency, current, active power, and load
- Battery condition, status, charge state, capacity, voltage, and estimated runtime
- Time running on battery
- Self-test result and details
- Delta UPSv5 alarm summary and individual critical alarms
- Configurable thresholds through macros
- Three graphs and an overview dashboard
- Numeric OIDs: installing MIB files on the Zabbix server is not required

### Compatibility

- Zabbix 7.0
- Delta InsightPower G3 Mini SNMP Card
- SNMPv2c
- Delta enterprise OID: `1.3.6.1.4.1.2254.2.5`
- Initially validated with UPS model `UPA302R2RX0B0B1` (3000 VA / 2700 W, single-phase)

### Installation

1. Download the English template from `templates/template_delta_insightpower_g3_en.yaml`.
2. In Zabbix, open **Data collection → Templates → Import**.
3. Import the YAML file.
4. Create a host and add an SNMP interface.
5. Configure the device IP, UDP port 161, SNMPv2, and its read-only community.
6. Link **Delta UPS InsightPower G3 Mini SNMP Card by SNMP - English**.

See [Installation guide](docs/installation.md) and [Monitored items](docs/monitored-items.md).

## Português

Template comunitário para Zabbix 7.0 destinado ao monitoramento de nobreaks Delta equipados com a placa **InsightPower G3 Mini SNMP Card**, utilizando SNMPv2c.

### Recursos

- Identificação do nobreak e da placa SNMP
- Tensão e frequência de entrada
- Tensão, frequência, corrente, potência ativa e carga da saída
- Condição, estado, carregamento, capacidade, tensão e autonomia da bateria
- Tempo de operação em bateria
- Resultado e detalhes do autoteste
- Resumo de alarmes UPSv5 e alarmes críticos individuais
- Limites configuráveis por macros
- Três gráficos e painel de visão geral
- OIDs numéricos, sem necessidade de instalar as MIBs no Zabbix

### Instalação

1. Baixe `templates/template_delta_insightpower_g3_pt_BR.yaml`.
2. No Zabbix, acesse **Coleta de dados → Templates → Importar**.
3. Importe o arquivo YAML.
4. Crie o host e adicione uma interface SNMP.
5. Configure IP, porta UDP 161, SNMPv2 e a community somente leitura.
6. Vincule **Delta UPS InsightPower G3 Mini SNMP Card by SNMP**.

## MIB references

The template was mapped from the vendor-provided `UPSv5.mib` and cross-checked against RFC 1628. Vendor MIB files are not redistributed in this repository and are not covered by the MIT License.

## Security

Use a read-only SNMP community, restrict UDP/161 access to the Zabbix server or proxy, and avoid committing credentials to this repository.

## License

The original template and documentation in this repository are licensed under the [MIT License](LICENSE). Delta product names and vendor MIB definitions remain the property of their respective owners.
