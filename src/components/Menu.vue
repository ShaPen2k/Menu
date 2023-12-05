<!--src/components/Menu.vue-->

<template>
  <div>
    <ul>
      <li v-for="item in menuItems" :key="item.id">
        {{ item.text }}
      </li>
    </ul>
    <button>Войти в личный кабинет</button>
  </div>
  <footer>
    <div class="footer-content">
      <div class="contact-info">
        <p>Телефон: {{ phoneNumber }}</p>
        <p>Юридический адрес: {{ legalAddress }}</p>
      </div>
      <div class="social-links">
        <a
          href="ссылка_на_ваш_facebook"
          target="_blank"
          rel="noopener noreferrer"
          ><img
            src="src/components/SVG color/Facebook.svg"
            width="20"
            height="18"
          />
          Facebook</a
        >
        <a
          href="ссылка_на_ваш_twitter"
          target="_blank"
          rel="noopener noreferrer"
          ><img
            src="src/components/SVG color/Snapchat.svg"
            width="20"
            height="18"
          />
          Snapchat</a
        >
        <a
          href="ссылка_на_ваш_twitter"
          target="_blank"
          rel="noopener noreferrer"
        >
          <img
            src="src/components/SVG color/Telegram.svg"
            width="20"
            height="18"
          />
          Telegram</a
        >
        <a
          href="ссылка_на_ваш_twitter"
          target="_blank"
          rel="noopener noreferrer"
        >
          <img
            src="src/components/SVG color/YouTube.svg"
            width="20"
            height="18"
          />
          YouTube</a
        >
        <a
          href="ссылка_на_ваш_twitter"
          target="_blank"
          rel="noopener noreferrer"
          ><img
            src="src/components/SVG color/Behance.svg"
            width="20"
            height="18"
          />
          Behance</a
        >
        <a
          href="ссылка_на_ваш_twitter"
          target="_blank"
          rel="noopener noreferrer"
        >
          <img
            src="src/components/SVG color/WeChat.svg"
            width="20"
            height="18"
          />
          WeChat</a
        >

        <!-- Добавьте другие социальные сети по аналогии -->
      </div>
    </div>
    <p>&copy; 2023 ООО "Транзит". Все права защищены.</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        { id: 1, text: "Главная" },
        { id: 2, text: "Контакты" },
        { id: 3, text: "Поддержка" },
        { id: 4, text: "О нас" },
        { id: 5, text: "Справка" },
        { id: 6, text: "Блог" },
      ],
      phoneNumber: "+7 (951) 971-3838", // Замените на ваш номер телефона
      legalAddress: "Кондратьевский проспект 43, д.8", // Замените на ваш юридический адрес
    };
  },
};
</script>

<style scoped>
/* Стили, специфичные для этого компонента */
footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 30px;
  border-radius: 5px;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.contact-info {
  text-align: left;
}
.social-links {
  width: 100px;
  display: flex;
  flex-wrap: wrap;
  margin-right: 20px;
}
.social-links a {
  color: #fff;
  padding-bottom: 5px;
}

.social-links a:hover {
  text-decoration: underline;
}

button {
  padding: 10px;
  border: 1px solid #ccc;
  cursor: pointer;
  flex: 1; /* Распределяем пространство равномерно между элементами */
  font-weight: 600;
  position: absolute;
  bottom: 660px;
  left: 600px;
}
@counter-style marker-emoji {
  system: cyclic;
  symbols: "🍋" "🍎" "🍒";
  suffix: " ";
}
ul {
  padding: 0;
  margin: 0px 600px 50px 0px;
  margin-bottom: 600px;
  display: flex;
  background-color: #eee;
  border-radius: 5px;
  flex-wrap: wrap; /* Добавляем поддержку переноса элементов на новую строку */
  list-style: none;
}

li {
  padding: 10px;
  border-right: 1px solid #ccc;
  border-bottom: 1px solid #ccc;
  cursor: pointer;
  flex: 1; /* Распределяем пространство равномерно между элементами */
  font-weight: 600;
}

li:last-child {
}

/* Добавляем стили для адаптивности */
@media (max-width: 600px) {
  li {
    border-bottom: 1px solid #ccc;
    border-right: none;
    border-bottom: none;
  }
}
</style>
