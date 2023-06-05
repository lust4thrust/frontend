<script lang="ts">
  import { mdiFacebook, mdiInstagram, mdiYoutube } from '@mdi/js'
</script>

<div class="root">
  <a href="/">
    <div class="logo" />
  </a>
  <a class="link" href="https://youtube.com/@lust4thrust" target="_blank">
    <svg class="icon">
      <path d={mdiYoutube} />
    </svg>
  </a>
  <a class="link" target="_blank" href="https://www.facebook.com/lustforthrust">
    <svg class="icon">
      <path d={mdiFacebook} />
    </svg>
  </a>
  <a class="link" href="https://instagram.com/lust4thrust" target="_blank">
    <svg class="icon">
      <path d={mdiInstagram} />
    </svg>
  </a>
  <div class="contact">
    <button class="button primary"> Contact </button>
  </div>
</div>

<style>
  .root {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
    width: 100%;
  }

  .logo {
    background-image: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjwhLS0gQ3JlYXRlZCB3aXRoIElua3NjYXBlIChodHRwOi8vd3d3Lmlua3NjYXBlLm9yZy8pIC0tPgoKPHN2ZwogICB3aWR0aD0iMzIwIgogICBoZWlnaHQ9IjMyMCIKICAgaWQ9InN2ZzIiCiAgIHZlcnNpb249IjEuMSIKICAgaW5rc2NhcGU6dmVyc2lvbj0iMS4xIChjNjhlMjJjMzg3LCAyMDIxLTA1LTIzKSIKICAgc29kaXBvZGk6ZG9jbmFtZT0ibHVzdDR0cnVzdC5zdmciCiAgIGlua3NjYXBlOmV4cG9ydC1maWxlbmFtZT0iL3Vzci9ob21lL21la2EvRmlsZXMvbHVzdDR0cnVzdC5wbmciCiAgIGlua3NjYXBlOmV4cG9ydC14ZHBpPSI5NiIKICAgaW5rc2NhcGU6ZXhwb3J0LXlkcGk9Ijk2IgogICB4bWxuczppbmtzY2FwZT0iaHR0cDovL3d3dy5pbmtzY2FwZS5vcmcvbmFtZXNwYWNlcy9pbmtzY2FwZSIKICAgeG1sbnM6c29kaXBvZGk9Imh0dHA6Ly9zb2RpcG9kaS5zb3VyY2Vmb3JnZS5uZXQvRFREL3NvZGlwb2RpLTAuZHRkIgogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiAgIHhtbG5zOnN2Zz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiAgIHhtbG5zOnJkZj0iaHR0cDovL3d3dy53My5vcmcvMTk5OS8wMi8yMi1yZGYtc3ludGF4LW5zIyIKICAgeG1sbnM6Y2M9Imh0dHA6Ly9jcmVhdGl2ZWNvbW1vbnMub3JnL25zIyIKICAgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIj4KICA8ZGVmcwogICAgIGlkPSJkZWZzNCIgLz4KICA8c29kaXBvZGk6bmFtZWR2aWV3CiAgICAgaWQ9ImJhc2UiCiAgICAgcGFnZWNvbG9yPSIjZmZmZmZmIgogICAgIGJvcmRlcmNvbG9yPSIjNjY2NjY2IgogICAgIGJvcmRlcm9wYWNpdHk9IjEuMCIKICAgICBpbmtzY2FwZTpwYWdlb3BhY2l0eT0iMCIKICAgICBpbmtzY2FwZTpwYWdlc2hhZG93PSIyIgogICAgIGlua3NjYXBlOnpvb209IjAuNDk0OTc0NzUiCiAgICAgaW5rc2NhcGU6Y3g9IjE1NC41NTMzNCIKICAgICBpbmtzY2FwZTpjeT0iMjE0LjE1MjM0IgogICAgIGlua3NjYXBlOmRvY3VtZW50LXVuaXRzPSJweCIKICAgICBpbmtzY2FwZTpjdXJyZW50LWxheWVyPSJsYXllcjEiCiAgICAgc2hvd2dyaWQ9ImZhbHNlIgogICAgIGlua3NjYXBlOndpbmRvdy13aWR0aD0iMTM2MiIKICAgICBpbmtzY2FwZTp3aW5kb3ctaGVpZ2h0PSI3MjkiCiAgICAgaW5rc2NhcGU6d2luZG93LXg9IjAiCiAgICAgaW5rc2NhcGU6d2luZG93LXk9IjE4IgogICAgIGlua3NjYXBlOndpbmRvdy1tYXhpbWl6ZWQ9IjEiCiAgICAgaW5rc2NhcGU6cGFnZWNoZWNrZXJib2FyZD0iMCIKICAgICBmaXQtbWFyZ2luLXRvcD0iMCIKICAgICBmaXQtbWFyZ2luLWxlZnQ9IjAiCiAgICAgZml0LW1hcmdpbi1yaWdodD0iMCIKICAgICBmaXQtbWFyZ2luLWJvdHRvbT0iMCIKICAgICB3aWR0aD0iMzIwcHgiIC8+CiAgPG1ldGFkYXRhCiAgICAgaWQ9Im1ldGFkYXRhNyI+CiAgICA8cmRmOlJERj4KICAgICAgPGNjOldvcmsKICAgICAgICAgcmRmOmFib3V0PSIiPgogICAgICAgIDxkYzpmb3JtYXQ+aW1hZ2Uvc3ZnK3htbDwvZGM6Zm9ybWF0PgogICAgICAgIDxkYzp0eXBlCiAgICAgICAgICAgcmRmOnJlc291cmNlPSJodHRwOi8vcHVybC5vcmcvZGMvZGNtaXR5cGUvU3RpbGxJbWFnZSIgLz4KICAgICAgPC9jYzpXb3JrPgogICAgPC9yZGY6UkRGPgogIDwvbWV0YWRhdGE+CiAgPGcKICAgICBpbmtzY2FwZTpsYWJlbD0iTGF5ZXIgMSIKICAgICBpbmtzY2FwZTpncm91cG1vZGU9ImxheWVyIgogICAgIGlkPSJsYXllcjEiCiAgICAgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTI1My41MDk1LC0zNTEuMDQ0NzYpIj4KICAgIDxwYXRoCiAgICAgICBzdHlsZT0iZm9udC1zdHlsZTpub3JtYWw7Zm9udC13ZWlnaHQ6bm9ybWFsO2ZvbnQtc2l6ZTo0MjMuNTU4cHg7bGluZS1oZWlnaHQ6MTI1JTtmb250LWZhbWlseTpTYW5zO2xldHRlci1zcGFjaW5nOjBweDt3b3JkLXNwYWNpbmc6MHB4O2ZpbGw6bm9uZTtzdHJva2U6I2ZmMDAwMDtzdHJva2Utd2lkdGg6MTUuMjtzdHJva2UtbWl0ZXJsaW1pdDo0O3N0cm9rZS1kYXNoYXJyYXk6bm9uZTtzdHJva2Utb3BhY2l0eToxIgogICAgICAgZD0ibSAzNzMuODY1NjYsMzc1LjY4MDExIGMgLTczLjM2MDMsMjEwLjgzNDI3IC0yMC40MTY5NSw1OC42Nzc0MiAtNjcuNzg4MzQsMTk0LjgyMDcyIGggNzcuOTM3NSBMIDM2MC4xMTczOSw2MzkuMTgxIGggNDQuNTYyNDkgbCAyMy44OTc0MywtNjguNjgwMTcgaCA0OS4xODI4OSBsIDEyLjEyMzk3LC0zNC44NDM3NSBoIC00OS4xODI4OSBsIDE2Ljk3MzU2LC00OC43ODEyNSBoIDc5Ljk0NzAxIGwgMTIuNjc4NTEsLTM2LjQzNzUgSCAzOTAuMDA5NiBsIDI2LjAxMjMxLC03NC43NTgyMiB6IG0gMy40NjU0MywxMTEuMTk1NzIgaCAzNS43ODEyNSBsIC0xNi45NzM1Niw0OC43ODEyNSBoIC0zNS43ODEyNSB6IgogICAgICAgaWQ9InRleHQzOTcyIgogICAgICAgaW5rc2NhcGU6Y29ubmVjdG9yLWN1cnZhdHVyZT0iMCIKICAgICAgIHNvZGlwb2RpOm5vZGV0eXBlcz0iY2NjY2NjY2NjY2NjY2NjY2NjY2MiCiAgICAgICBpbmtzY2FwZTpleHBvcnQtZmlsZW5hbWU9Ii91c3IvaG9tZS9tZWthL0ZpbGVzL2x1c3Q0dHJ1c3QucG5nIgogICAgICAgaW5rc2NhcGU6ZXhwb3J0LXhkcGk9Ijk2IgogICAgICAgaW5rc2NhcGU6ZXhwb3J0LXlkcGk9Ijk2IiAvPgogIDwvZz4KPC9zdmc+Cg==);
    background-size: 100% 100%;
    width: 26px;
    margin-right: 10px;
    height: 26px;
  }

  .link {
    width: 26px;
    height: 26px;
    margin-right: 10px;
  }

  .icon {
    width: 26px;
    height: 26px;
    fill: red;
  }

  .contact {
    flex: 1;
    display: flex;
    justify-content: flex-end;
  }
</style>
