<script>
import axios from "axios";

export default {
  name: "BlockBusiness",
  components: {},
  data() {
    return {
      lang: "RU",
      cards_ru: [
        {
          qst: "Что такое Bitcoin?",
          ans: `<p>
          <b>Bitcoin (BTC)</b> — это первый и наиболее известный криптовалютный актив, основанный на технологии blockchain. Он был представлен в виде открытого исходного кода в 2008 году, а его разработка была завершена в январе 2009 года. Основателем Bitcoin является неизвестный программист под псевдонимом Satoshi Nakamoto.</p>`,
          open: false,
        },
        {
          qst: "Что такое майнинг и почему это выгодно?",
          ans: `<p>
          <b>Майнинг</b> — это процесс обработки и подтверждения транзакций в
          сети криптовалют, при котором новые блоки добавляются к блокчейну.
          Майнеры используют мощные специализированные компьютеры для решения
          сложных математических задач, и тот, кто первым решит задачу, получает
          вознаграждение в виде новых биткоинов. Это механизм, который
          одновременно выпускает новые биткоины и поддерживает работу сети
          благодаря верификации и записи транзакций. Почему майнинг может
          считаться лучшей инвестицией в Bitcoin? Больше Bitcoin на вложенные
          деньги: Главная причина, по которой майнинг является лучшей
          инвестицией в Bitcoin очень простая - за тот же объем инвестиций
          майнер в перспективе получает большее количество Bitcoin, чем при
          покупке на бирже. Оборудование растет в цене вместе с Bitcoin: Цены на
          оборудование для майнинга зависят от его доходности, а доходность - от
          цены Bitcoin. Таким образом с ростом цены на заработанный Bitcoin
          растет и стоимость оборудования, майнинг как бы удваивает вашу ставку
          на рост цены Bitcoin. Пассивный доход: После первоначальных инвестиций
          в оборудование майнеры могут регулярно получать биткоины в качестве
          вознаграждения. Поддержка инфраструктуры: Майнеры способствуют
          безопасности сети Bitcoin, что в свою очередь может повысить доверие к
          этой криптовалюте.
        </p>`,
          open: false,
        },
        {
          qst: "Почему важно начать майнинг Bitcoin сейчас?",
          ans: `<p>Начало майнинга биткоина сейчас может принести значительные финансовые выгоды, учитывая текущий рост стоимости и спроса на биткоин.</p>`,
          open: false,
        },
        {
          qst: "Что такое Mining Pool?",
          ans: `<p><b>Mining Pool</b> — это группа криптовалютных майнеров, которые объединяют свои ресурсы для увеличения своих шансов на получение вознаграждения за открытие нового блока в блокчейне. Майнинг блока требует значительных вычислительных ресурсов и времени, поэтому объединение усилий в пуле позволяет майнерам более эффективно использовать свои мощности и увеличить вероятность получения вознаграждения.</p>`,
          open: false,
        },
      ],
      cards_en: [
        {
          qst: "What is Bitcoin?",
          ans: `<p>
          <b>Bitcoin (BTC)</b> — this is the first and most well-known cryptocurrency asset based on blockchain technology. It was introduced as open source in 2008, and its development was completed in January 2009. The founder of Bitcoin is an unknown programmer under the pseudonym Satoshi Nakamoto.</p>`,
          open: false,
        },
        {
          qst: "What is mining and why is it profitable?",
          ans: `<p>
<b>Mining</b> is the process of processing and confirming transactions in
the cryptocurrency network, in which new blocks are added to the blockchain.
          Miners use powerful specialized computers to solve
          complex mathematical problems, and the one who solves the problem first gets
          The reward is in the form of new bitcoins. This is a mechanism that
          at the same time, it releases new bitcoins and supports the operation of the network
          thanks to the verification and recording of transactions. Why mining can
          be considered the best investment in Bitcoin? More Bitcoin for nested
          Money: The main reason mining is the best
          investing in Bitcoin is very simple - for the same amount of investment
          In the future, the miner receives a larger amount of Bitcoin than when
buying on the stock exchange. Hardware grows in price along with Bitcoin: The prices of
mining equipment depend on its profitability, and profitability depends on
          Bitcoin prices. Thus, with the increase in the price of earned Bitcoin
          The cost of equipment is also increasing, mining doubles your bet
          the rise in the price of Bitcoin. Passive income: After initial investment
          in the hardware, miners can regularly receive bitcoins as
          rewards. Infrastructure support: Miners contribute
          the security of the Bitcoin network, which in turn can increase trust in
          this cryptocurrency.
        </p>`,
          open: false,
        },
        {
          qst: "Why is it important to start mining Bitcoin now?",
          ans: `<p>Starting bitcoin mining now can bring significant financial benefits, given the current growth in the value and demand for bitcoin.</p>`,
          open: false,
        },
        {
          qst: "What is a Mining Pool?",
          ans: `<p><b>Mining Pool</b> is a group of cryptocurrency miners who pool their resources to increase their chances of receiving rewards for opening a new block in the blockchain. Mining a block requires significant computing resources and time, so pooling efforts allows miners to use their power more efficiently and increase the likelihood of receiving rewards.</p>`,
          open: false,
        },
      ],
      cards_he: [
        {
          qst: "מה זה Bitcoin?",
          ans: `<p>
          <b> Bitcoin (BTC)</b> הוא נכס הקריפטו הראשון והידוע ביותר המבוסס על טכנולוגיית blockchain. הוא הוצג כקוד פתוח בשנת 2008, ופיתוחו הושלם בינואר 2009. מייסד Bitcoin הוא מתכנת לא ידוע תחת שם בדוי Satoshi Nakamoto.</p>`,
          open: false,
        },
        {
          qst: "מהי כרייה ומדוע היא רווחית?",
          ans: `<p>
          <b> כרייה</b> הוא תהליך עיבוד ואישור עסקאות ב
          רשתות cryptocurrency, בהן מתווספות חסימות חדשות לבלוקצ ' יין.
          כורים משתמשים במחשבים מיוחדים רבי עוצמה כדי לפתור
          של בעיות מתמטיות מורכבות, ומי שפותר את הבעיה תחילה מקבל
          תגמול בצורה של ביטקוין חדש. זה המנגנון ש
          במקביל משחרר ביטקוין חדש ושומר על הרשת
          באמצעות אימות ורישום עסקאות. מדוע כרייה יכולה
          נחשב להשקעה הטובה ביותר בביטקוין? עוד Bitcoin על מקונן
          כסף: הסיבה העיקרית לכרייה היא הטובה ביותר
          השקעה בביטקוין היא פשוטה מאוד - עבור אותה כמות השקעה
          כורה בפרספקטיבה מקבל כמות גדולה יותר של Bitcoin מאשר עם
          לקנות בבורסה. החומרה עולה במחיר יחד עם Bitcoin: מחירי
          ציוד הכרייה תלוי בתשואה שלו, והתשואה תלויה ב
          מחירי Bitcoin. לפיכך, עם עליית המחיר של bitcoin הרוויח
          גם עלות הציוד עולה, הכרייה מכפילה את ההימור שלך
          על עליית מחיר Bitcoin. הכנסה פסיבית: לאחר השקעה ראשונית
          בציוד, כורים יכולים לקבל ביטקוין באופן קבוע כ
          תגמולים. תמיכה בתשתית: כורים תורמים
          אבטחת רשת Bitcoin, אשר בתורו יכול לשפר את האמון
          מטבע מבוזר זה.
        </p>`,
          open: false,
        },
        {
          qst: "למה חשוב להתחיל כריית Bitcoin עכשיו?",
          ans: `<p> תחילת כריית ביטקוין כעת יכולה להביא יתרונות פיננסיים משמעותיים, בהתחשב בעלייה הנוכחית בערך ובביקוש לביטקוין.</p>`,
          open: false,
        },
        {
          qst: "מהי בריכת כרייה?",
          ans: `<p> <b>Mining Pool</b> היא קבוצה של כורי מטבעות קריפטוגרפיים המאגדים את המשאבים שלהם כדי להגדיל את סיכוייהם לקבל תגמול על פתיחת בלוק חדש בבלוקצ ' יין. כריית חסימות דורשת משאבי מחשוב וזמן משמעותיים, ולכן איחוד כוחות בבריכה מאפשר לכורים להשתמש בכוחותיהם בצורה יעילה יותר ולהגדיל את הסבירות לקבל תגמולים.</p>`,
          open: false,
        },
      ],
      cards: [],
    };
  },
  methods: {
    goCreate() {
      let token = localStorage.getItem("token");
      if (token) {
        this.$router.push({ name: "createTicket" });
      } else {
        this.$emit("updateLogin", true);
      }
    },
    goTickets() {
      let token = localStorage.getItem("token");
      if (token) {
        this.$router.push({ name: "tickets" });
      } else {
        this.$emit("updateLogin", true);
      }
    },
  },
  async mounted() {
    try {
      let id = localStorage.getItem("id");
      if (id) {
        let response = await axios.get(`/users/${id}`, {
          headers: {
            Authorization: `Bearer ${localStorage.getItem("token")}`,
          },
        });
        this.lang = response.data.user.lang;
      } else {
        setInterval(() => {
          this.lang = localStorage.getItem("lang");
          if (this.lang == "RU") {
            this.cards = this.cards_ru;
          } else if (this.lang == "EN") {
            this.cards = this.cards_en;
          } else if (this.lang == "HE") {
            this.cards = this.cards_he;
          } else {
            this.cards = this.cards_ru;
          }
        }, 1000);
      }
      if (this.lang == "RU") {
        this.cards = this.cards_ru;
      } else if (this.lang == "EN") {
        this.cards = this.cards_en;
      } else if (this.lang == "HE") {
        this.cards = this.cards_he;
      } else {
        this.cards = this.cards_ru;
      }
    } catch (err) {
      console.log(err);
    }
  },
};
</script>
<template>
  <div class="wrapper">
    <div class="wrap-title">
      <h2>FAQ</h2>
      <div class="wrap-btns" v-if="$route.name == 'support'">
        <button @click="goCreate" class="btn">{{ $t("createTicket") }}</button>
        <button @click="goTickets" class="btn myTickets">
          {{ $t("myTickets") }}
        </button>
      </div>
    </div>
    <div class="cards">
      <div
        class="card"
        v-for="card in cards"
        :key="card"
        @click="card.open = !card.open"
        :class="{ active: card.open }"
      >
        <div class="info">
          <span class="qst">{{ card.qst }}</span>
          <img
            v-if="!card.open"
            class="arr"
            src="../assets/arrow-down.png"
            alt=""
          />
          <img
            v-if="card.open"
            class="arr rot"
            src="../assets/arrow-down.png"
            alt=""
          />
        </div>
        <div v-if="card.open" class="ans" v-html="card.ans"></div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  width: 100%;
  margin-top: 40px;
  padding: 0 40px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.wrap-title {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.btn {
  background-color: #cf0032;
  color: #fff;
  border: 1px solid #cf0032;
  border-radius: 10px;
  padding: 12px 17px;
  width: 224px;
  height: 50px;
  font-weight: 500;
  font-size: 16px;
  line-height: 16px;
}

.cards {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card {
  cursor: pointer;
  width: 100%;
  padding: 30px;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card:hover {
  transform: scale(1.02);
}

.info {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: row;
}

.arr {
  width: 24px;
  height: 24px;
}

.rot {
  transform: rotate(180deg);
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.ans {
  animation-name: fade-in;
  animation-duration: 0.5s; /* Задержка анимации */
  animation-fill-mode: forwards; /* Элемент останется в состоянии после окончания анимации */
}

.qst {
  font-weight: 600;
  font-size: 24px;
  line-height: 24px;
  color: #0f0f0f;
}

.active {
  transform: scale(1.02);

  transition: all 500ms ease;
}

.wrap-btns {
  display: flex;
  flex-direction: column;
  gap: 7px;
}

.myTickets {
  background-color: transparent;
  border: 1px solid #cf0032;
  color: #cf0032;
}
</style>
