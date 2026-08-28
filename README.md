![img](logo.png)

## Docs
- [https://helved-docs.ansatt.dev.nav.no](https://helved-docs.ansatt.dev.nav.no) Repo: [helved-docs](https://github.com/navikt/helved-docs)
- [intern doc](https://github.com/navikt/helved-utbetaling/tree/main/dokumentasjon)
- [Team Audit Logs](TEAM_AUDIT_LOGS.md)

## Apps
- [helved-utbetaling](https://github.com/navikt/helved-utbetaling)
  * [abetal](https://github.com/navikt/helved-utbetaling/tree/main/apps/abetal)
  * [peisschtappern](https://github.com/navikt/helved-utbetaling/tree/main/apps/peisschtappern) 
  * [simulering](https://github.com/navikt/helved-utbetaling/tree/main/apps/simulering)
  * [urskog](https://github.com/navikt/helved-utbetaling/tree/main/apps/urskog)
  * [utsjekk](https://github.com/navikt/helved-utbetaling/tree/main/apps/utsjekk)
  * [vedskiva](https://github.com/navikt/helved-utbetaling/tree/main/apps/vedskiva)
- [helved-peisen](https://github.com/navikt/helved-peisen)
- [helved-ws-proxy](https://github.com/navikt/helved-ws-proxy)
- [helved-performance](https://github.com/navikt/helved-performance)

## Libs
- [helved-utbetaling](https://github.com/navikt/helved-utbetaling/tree/main/libs)
- [helved-libs](https://github.com/navikt/helved-libs)

## Tools
- [https://peisen.intern.dev.nav.no](https://peisen.intern.dev.nav.no/)
- [https://peisen.intern.nav.no](https://peisen.intern.nav.no/)
- [helved-kafka-cli](https://github.com/navikt/helved-kafka-cli)

### trace-logs
depends on `gcloud`, `logcli`, `tempo-cli`.

logcli kan installeres fra homebrew,

tempo-cli må muligens bygges selv (https://github.com/grafana/tempo),
pass på at binary som bygges heter `tempo-cli-arm64` og er tilgjengelig på PATH.

