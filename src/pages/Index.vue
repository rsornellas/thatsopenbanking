<template>
  <Layout>
    <section>
      <video
        src="../assests/videoplayback.mp4"
        autoplay
        muted
        loop
        :style="{ opacity: this.opacity }"
      ></video>
    </section>

    <section>
      <div class="content">
        <h1>O que é Open Banking?</h1>

        <h2>
          Open Banking é uma das promessas de grande mudança e impacto no
          mercado financeiro.
        </h2>

        <p>
          O nome pode parecer diferente, mas você já deve ter visto por aí. Open
          Banking é uma das promessas de grande mudança e impacto no mercado
          financeiro. Na tradução literal, significa “banco aberto” e é ótimo
          para todos os consumidores. <br />
          <br />
          É basicamente um novo movimento que permite a integração das chamadas
          de interface de programação de aplicativos (API, na sigla em inglês).
          Na prática, parte do entendimento de que os dados bancários pertencem
          aos clientes e não às instituições. Ótimo, não é mesmo? Isso garante
          autonomia e aumenta a oferta de produtos e serviços, já que você pode
          ter e pegar todas as suas informações e levá-las para onde quiser, sem
          ter que começar a conversa do zero com a sua nova instituição
          financeira. <br />
          <br />
          Essa já é uma realidade no Reino Unido e em outros lugares. No Brasil,
          o Banco Central mantém algumas discussões sobre regras e
          funcionamentos. Mas, o legal é que já existem muitas instituições
          tradicionais e fintechs que estão participando dessa próxima onda de
          evolução de tecnologia para as instituições financeiras.
        </p>

        <h1>Benefícios do Open Banking</h1>

        <h2>
          Com o sistema de arquitetura aberta, pessoas e mercado têm mais
          oportunidades.
        </h2>

        <p>
          O Open Banking parte da premissa de que os dados financeiros são das
          pessoas, e não devem ficar restritos aos bancos.
          <br />
          <br />

          Hoje, os bancos que operam sob o modelo de arquitetura fechada mantêm
          os dados restritos a um lugar em que apenas eles têm acesso. Os
          consumidores só têm alcance a informações como extratos, saldos e
          afins, de forma limitada. O Open Banking age para “abrir” esse
          sistema, além de possibilitar que as empresas permitam o acesso as
          suas interfaces de programação, para o desenvolvimento de aplicações
          por parte de outras empresas, ao que chamamos de API (Application
          Programming Interface).
          <br />
          <br />

          Mas, isso significa que se o Open Banking operar de forma plena
          qualquer um terá acesso aos dados? Não. As instituições vão precisar
          da autorização expressa de cada consumidor para poder usar os dados em
          operações financeiras diversas – pedidos de empréstimos, abertura de
          contas, financiamentos, seguros, previdência, investimentos, etc.
          <br />
          <br />

          Por exemplo: uma pessoa deseja um financiamento em um banco/fintech X,
          mas só consegue comprovar sua renda pelas últimas movimentações
          bancárias que mantém com o banco tradicional Y. Para ir além, precisa
          ir até o banco, enfrentar filas, falar com o gerente... Com o Open
          Banking, o banco Y será obrigado a fornecer os dados para a
          instituição financeira X, com a autorização do cliente, sem que ele se
          veja obrigado a enfrentar burocracias.
          <br />
          <br />

          Nesse caso, o consumidor terá mais autonomia para poder usufruir de
          diversos produtos e serviços financeiros, de várias instituições. O
          Open Banking também viabiliza a integração dos sistemas dos bancos com
          fintechs e a automatização de uma série de transações.
          <br />
          <br />

          <a
            href="https://www.bcb.gov.br/conteudo/home-ptbr/TextosApresentacoes/Open%20Banking%20-%20V07%20-%20Evento%20C4%20-%20S%C3%A3o%20Paulo.pdf"
            >Nesta apresentação</a
          >
          divulgada pelo Banco Central há mais informações detalhando como
          ocorrerá a implementação do Open Banking no Brasil.
        </p>

        <h3>Com a concorrência, ampliam-se as oportunidades</h3>

        <p>
          A abertura das informações e uma conexão entre as instituições
          financeiras vai aumentar a concorrência entre elas. Assim, os
          consumidores poderão encontrar no mercado opções mais atrativas e
          menos abusivas em relação a taxas diversas na solicitação de alguns
          produtos e serviços e até quando optar pela portabilidade, como já é
          praticado por bancos e fintechs que operam no mercado.
          <br />
          <br />
          Aqui na Franq temos parcerias com bancos e fintechs que agem de acordo
          com o Open Banking. Encontre um Personal Banker para saber mais!
        </p>

        <h3>E como a Franq utiliza isso?</h3>

        <p>
          Existem muitas opções e possibilidades no mercado financeiro, certo?
          Vários cartões de crédito, várias contas digitais, vários
          investimentos... e como saber qual o melhor para a sua vida? Na Franq
          utilizamos o sistema de Open Banking para apresentar as ofertas e
          propostas dos parceiros, para que você tenha um leque de opções para
          comparar e decidir.
        </p>

        <h3>Ok, vocês são um comparador de produtos então?</h3>

        <p>
          Não. O nosso grande diferencial é o fato de que usamos desse recurso
          de Open Banking, mas não nos limitamos a solução digital. Nosso
          atendimento é humano, real e pessoal e ocorre pela orientação de
          bancários fora do mercado de trabalho e que agora são Personal
          Bankers. Os Personal Bankers são profissionais que trabalharam por
          vários anos em grandes instituições bancárias, por isso, possuem uma
          alta capacidade e conhecimento para poder dizer se o cartão X é o
          melhor caminho para você. A melhor parte é que eles não possuem metas
          ou pressões dos grandes bancos (que induzem os vendedores a oferecer
          um produto em especial, independentemente da necessidade dos clientes)
          e você poderá contar com essa expertise de forma gratuita. Pronto para
          descobrir este movimento de mudança? Procure um
          <a href="https://www.franq.com.br/busca?page=busca"
            >Personal Banker</a
          >
          e conheça mais.
        </p>
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "O que é Openbanking",
  },
  data() {
    return {
      opacity: 1,
      mobile: false,
    };
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);

    if (screen.width < 600) this.mobile = true;
  },
  methods: {
    handleScroll(event) {
      let divider = this.mobile ? -300 : -700;

      this.opacity = 1 + window.scrollY / divider;
    },
  },
};
</script>

<style>
section {
  position: relative;
  width: 100%;
  min-width: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

section video {
  width: 100%;
  height: 100%;
  pointer-events: none;
  box-sizing: border-box;
}

.content {
  padding: 100px 300px 0px 300px;
}

a {
  color: #677cea;
  text-decoration-color: #677cea;
  text-decoration: none;
}

section h1 {
  color: #fff;
  font-size: 4em;
  margin-bottom: 100px;
  text-align: center;
}

section h2 {
  color: #fff;
  font-size: 3em;
  margin-bottom: 60px;
}

section h3 {
  color: #fff;
  font-size: 2em;
  margin-bottom: 60px;
}

section p {
  position: relative;
  color: #fff;
  font-size: 1.2em;
  margin-bottom: 50px;
}

@media screen and (max-width: 600px) {
  .content {
    padding: 50px;
  }

  section h1 {
    font-size: 3.2em;
    margin-bottom: 60px;
  }

  section h2 {
    font-size: 2em;
    margin-bottom: 30px;
  }

  section h3 {
    font-size: 1.8em;
    margin-bottom: 20px;
  }

  section p {
    font-size: 1.4em;
    margin-bottom: 25px;
  }
}
</style>
