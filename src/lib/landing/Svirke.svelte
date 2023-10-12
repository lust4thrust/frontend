<div class="root">
  <div class="content">
    <h2 class="title">Svirke</h2>
    <div class="svirka">
      <div class="datum">
        <div class="dan">14</div>
        <div class="mesec">OCT</div>
      </div>
      <div class="mesto">
        <div class="naziv">Distorded Minds</div>
        <div>CK13, Vojvode Bojovića 13, Novi Sad</div>
      </div>
      <div class="mapa">
        <a
          href="https://www.openstreetmap.org/?mlat=45.25829&mlon=19.84005#map=19/45.25829/19.84005"
          target="_blank"
        >
          Mapa
        </a>
      </div>
    </div>
    <hr />
    <div class="svirka">
      <div class="datum">
        <div class="dan">18</div>
        <div class="mesec">OCT</div>
      </div>
      <div class="mesto">
        <div class="naziv">Liman Zove</div>
        <div>Fabrika, Bulevar Despota Stefana 5, Novi Sad</div>
      </div>
      <div class="mapa">
        <a
          href="https://www.openstreetmap.org/?mlat=45.23756&mlon=19.84224#map=18/45.23756/19.84224"
          target="_blank"
        >
          Mapa
        </a>
      </div>
    </div>
    <hr />
    <div class="svirka">
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
          href="https://www.openstreetmap.org/?mlat=44.86924&mlon=20.63741#map=19/44.86924/20.63741"
          target="_blank"
        >
          Mapa
        </a>
      </div>
    </div>
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
