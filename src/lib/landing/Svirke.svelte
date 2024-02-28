<div class="root">
  <div class="content">
    <h2 class="title">Svirke</h2>
    <!-- div class="svirka">
      <div class="datum">
        <div class="dan">23</div>
        <div class="mesec">DEC</div>
      </div>
      <div class="mesto">
        <div class="naziv">Pančevo</div>
        <div>Bajka 013, Miladina Popovića 18, Pančevo</div>
      </div>
      <div class="mapa">
        <a
          href="https://www.openstreetmap.org/?mlat=44.87066&mlon=20.63577#map=19/44.87066/20.63577"
          target="_blank"
        >
          Mapa
        </a>
      </div>
    </div -->
    <hr />
  </div>
</div>

<style>
  .root {
    padding: 20px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .content {
    width: 100%;
    max-width: 1024px;
  }

  .title {
    text-align: center;
    font-size: 4rem;
    margin-bottom: 50px;
  }

  .svirka {
    display: flex;
  }

  .datum {
    text-align: center;
    justify-content: center;
    align-items: center;
    display: flex;
    flex-direction: column;
    margin-left: 10px;
  }

  .dan {
    margin: 0;
    padding: 0;
    font-size: 4rem;
    line-height: 4rem;
    text-align: center;
  }

  .mesec {
    color: var(--color-primary);
    font-size: 2rem;
    padding: 0px;
    margin: 0px;
    line-height: 2rem;
    text-align: center;
  }

  .mesto {
    flex: 1;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  .naziv {
    color: var(--color-primary);
    font-size: 2rem;
  }

  .mapa {
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
