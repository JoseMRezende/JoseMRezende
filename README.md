```console
$ java -jar jose-marcos.jar --spring.profiles.active=backend,mobile

       ______  _____ ______   __  ______    ____  __________  _____
      / / __ \/ ___// ____/  /  |/  /   |  / __ \/ ____/ __ \/ ___/
 __  / / / / /\__ \/ __/    / /|_/ / /| | / /_/ / /   / / / /\__ \
/ /_/ / /_/ /___/ / /___   / /  / / ___ |/ _, _/ /___/ /_/ /___/ /
\____/\____//____/_____/  /_/  /_/_/  |_/_/ |_|\____/\____//____/
====================================================================
 :: José Marcos Rezende Junior ::                  (v2.0.0-SNAPSHOT)

21:04:17.412  INFO 2026 --- [main] b.c.j.DevApplication     : Starting DevApplication using Java 25
21:04:17.415  INFO 2026 --- [main] b.c.j.DevApplication     : Profiles ativos: "backend", "mobile"
21:04:17.530  INFO 2026 --- [main] b.c.j.config.Perfil      : Nome ....... José Marcos Rezende Junior
21:04:17.531  INFO 2026 --- [main] b.c.j.config.Perfil      : Cargo ...... Desenvolvedor Java & Android
21:04:17.532  INFO 2026 --- [main] b.c.j.config.Perfil      : Empresa .... TURION Analysis System
21:04:17.533  INFO 2026 --- [main] b.c.j.config.Perfil      : Domínio .... Gestão têxtil - ERP
21:04:17.534  INFO 2026 --- [main] b.c.j.config.Perfil      : Formação ... ADS @ Facens (2022 - 2024)
21:04:18.101  INFO 2026 --- [main] b.c.j.config.JavaRuntime : JDKs carregados: 17, 21, 25
21:04:18.297  INFO 2026 --- [main] c.z.h.HikariDataSource   : HikariPool-1 - Start completed (PostgreSQL | H2)
21:04:18.642  INFO 2026 --- [main] liquibase.changelog      : Changelog aplicado. Schema versionado
21:04:18.910  INFO 2026 --- [main] o.s.a.r.c.RabbitMQ       : Created new connection: filas prontas
21:04:19.004  INFO 2026 --- [main] b.c.j.mobile.Android     : Módulo Android (Java/XML) inicializado
21:04:19.120  INFO 2026 --- [main] b.c.j.ai.AiConfig        : Integração com IA habilitada
21:04:19.233  WARN 2026 --- [main] b.c.j.infra.CafeMonitor  : Nível de café baixo. Reabastecendo...
21:04:19.380  INFO 2026 --- [main] o.s.b.w.e.t.TomcatWeb    : Tomcat started on port 8080 (http)
21:04:19.391  INFO 2026 --- [main] b.c.j.DevApplication     : Started DevApplication in 2.026 seconds
```

```console
$ curl -s localhost:8080/api/v1/stack
{
  "backend": ["Java 17 | 21 | 25", "Spring Boot", "RabbitMQ", "Liquibase"],
  "bancoDeDados": ["PostgreSQL", "H2 Database"],
  "mobile": ["Android", "Android Studio", "XML"]
}

$ curl -s localhost:8080/api/v1/contatos
{
  "linkedin": "https://www.linkedin.com/in/josemrjunior",
  "email": "jose.marcos.dev7@gmail.com"
}
```

<br/>

```console
^C
23:59:59.901  INFO 2026 --- [ionShutdownHook] o.s.b.w.e.t.GracefulShut : Commencing graceful shutdown...
23:59:59.950  INFO 2026 --- [ionShutdownHook] b.c.j.DevApplication     : Obrigado pela visita! Volte sempre.
23:59:59.999  INFO 2026 --- [ionShutdownHook] c.z.h.HikariDataSource   : HikariPool-1 - Shutdown completed.

Process finished with exit code 0
```
