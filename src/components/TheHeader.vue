<script></script>

<template>
  <header class="header">
    <div class="header__container">
      <div class="header__logo"><a href="#">билеты и абонементы</a></div>
      <nav class="header__navbar">
        <ul class="navbar__list">
          <li class="navbar__list_item">
            <a href="#">Как купить?</a>
          </li>
          <li class="navbar__list_item">
            <a href="#">Правила</a>
          </li>
          <li class="navbar__list_item">
            <a href="#">Возврат билетов</a>
          </li>
        </ul>
      </nav>
      <a href="#" class="btn-enter btn">Войти</a>
    </div>
  </header>
</template>

<style lang="scss">
.header {
  position: absolute;
  z-index: 100;
  width: 100%;
  &__container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    align-items: center;
    min-height: 100px;
    color: #fff;
    white-space: nowrap;
    font-size: 20px;
    a {
      color: #fff;
      text-decoration: none;
    }
  }
  &__logo {
    text-transform: uppercase;
    font-size: 25px;
  }
  &__navbar {
    width: 100%;
  }
}
.navbar {
  &__list {
		@include center;
    gap: 150px;
    &_item a{
			transition: .3s;
			&:hover {
				transition: .3s;
				color: darken(#fff, 30%);
			}
    }
  }
}
.btn-enter {
	position: relative;
	transition: .3s;
	&:hover {
		transition: .3s;
		color: darken(#fff, 30%);
	}
	&::before {
		@include pseudo;
		background: url("/public/logout.svg");
		background-size: 24px;
		width: 24px;
		height: 24px;
		position: absolute;
		left: -30px;
	}
}
</style>
