# A FAZER
- [x] Graylog, Mongo e Elastisearch
- [x] Configurar Timezone de Usuários
- [x] Cerebro para gerência Web do Elasticsearch
- [x] Grafana integrado ao Elasticsearch
- [x] Ativar GeoIP
- [ ] Validar GeoIP
- [ ] Validar Índices de acordo com a LGPD


# UMA ESBOÇO DE ESTRATÉGIA


Inspirado no artigo *[PLANNING YOUR LOG COLLECTION]*(https://docs.graylog.org/v1/docs/planning) podemos trabalhar com estratégias de rotação/retenção diferentes para cada classe de log, no caso usando os Índices do Graylog.

**Dados operacionais (métricas de sistema e tal):** rotacionar mais vezes (talvez semanalmente)

**Dados de tentativas de ataques externos:** rotacionar mensal, bimestral ou trimestral pra em situação de ataque, podemos ter um relatório de GeoIP e tudo mais

**Dados de  acessos se usuários(MAC/IP DHCP Leases, horário início/fim, login, etc):** esse sim, temos que seguir a LGPD e o Marco Civil, tenho quase certeza que pra nós é 1 ano de rotação