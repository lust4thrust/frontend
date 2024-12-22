<div class="root">
  <div class="content">
    <h2 class="title">O nama</h2>
    <div class="avatars">
      <div class="av mekoslav">
        <div class="avatar meka" />
        Meka - gitara
      </div>
      <div class="av">
        <div class="avatar nemanja" />
        Nemanja - bubnjevi
      </div>
      <div class="av ninoslav">
        <div class="avatar nino" />
        Nino - vokal
      </div>
      <div class="av">
        <div class="avatar pop" />
        Pop - gitara
      </div>
      <div class="av">
        <div class="avatar bane" />
        Bane - bas
      </div>
    </div>
    <p>
      Lust 4 Thrust je žestok bend iz Novog Sada, poznat po high gain zvuku,
      snažnim rifovima i agresivnom bubnju. Stilom su najbliži grunge zvuku, ali
      sa jačom distorzijom koja daje jedinstveni pečat. Bend je nastao 2019.
      godine u Novom Sadu, a nakon nekoliko izmena u sastavu ustalio se u
      formaciji koju čine Goran Mekić - Meka (gitara), Miloš Damnjanović - Pop
      (gitara), Nemanja Drljača (bubnjevi), Branislav Gudurić - Bane (bas) i
      Nino Tamindžija (vokal). Oni su uspešno stvorili svoj prepoznatljiv stil
      koji odlikuje high gain zvuk, stoner i grunge rifovi, agresivan bubanj,
      veoma raznovrstan vokal, kao i provokativni tekstovi.
    </p>
    <p>
      Prvi album pod nazivom "Da li si spremna za let?" donosi deset pesama koje
      obrađuju najrazličitije aktuelne teme kao što su nasilje nad ženama
      (Plen), religija (Ja sam tvoj Bog), stanje sistema u državi (Kriza
      morala), bolesti zavisnosti (Zver u tebi), ali i muško - ženskih odnosa
      (Da li si spremna za let?, Poslednji pozdrav).
    </p>
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

  .avatar {
    height: 200px;
    width: 200px;
    border-radius: 50%;
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }

  .meka {
    background-image: url('/img/meka.webp');
  }

  .nemanja {
    background-image: url('/img/nemanja.webp');
  }

  .nino {
    background-image: url('/img/nino.webp');
  }

  .pop {
    background-image: url('/img/pop.webp');
  }

  .bane {
    background-image: url('/img/bane.webp');
  }

  @media screen and (min-width: 1050px) {
    .avatars {
      display: grid;
      margin-bottom: 20px;
      grid-template-columns: auto auto auto auto auto;
    }

    .av {
      text-align: center;
      grid-row: 1;
    }

    .ninoslav {
      grid-row: 1;
      grid-column: 3;
    }

    .mekoslav {
      grid-column: 1;
    }
  }

  @media screen and (max-width: 1050px) {
    .avatars {
      display: grid;
      margin-bottom: 20px;
      grid-template-columns: auto auto auto;
    }

    .av {
      text-align: center;
    }

    .ninoslav {
      grid-row: 1;
      grid-column: 1;
    }

    .mekoslav {
      grid-row: 1;
      grid-column: 2;
    }
  }

  @media screen and (max-width: 650px) {
    .avatars {
      display: grid;
      margin-bottom: 20px;
      grid-template-columns: auto auto;
    }

    .av {
      text-align: center;
    }
  }

  @media screen and (max-width: 450px) {
    .avatars {
      display: grid;
      margin-bottom: 20px;
      grid-template-columns: auto;
      justify-items: center;
      align-items: center;
    }

    .av {
      text-align: center;
    }

    .ninoslav {
      grid-row: 1;
      grid-column: 1;
    }

    .mekoslav {
      grid-row: 2;
      grid-column: 1;
    }
  }
</style>
