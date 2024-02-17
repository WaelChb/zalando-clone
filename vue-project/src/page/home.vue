
<template>
    
    <div class="main">

        <div class="haut">
            <span> 
            
            <a href="/aide/Paiement/Essayez-d%27abord-payez-apres.html">Essayez d’abord, payez après </a>
        </span>
        <span title="*La livraison est gratuite pour les commandes supérieures à 34,00 €. Pour les commandes inférieures à ce montant, les frais de livraison sont de 4,95 €.">
            <a href="/aide/Expedition-and-Livraison/Frais-de-livraison.html" >Livraison standard offerte à partir de 34,00 € et retours gratuits*</a>
        </span>
        <span>
            <a href="/aide/Retour-and-Remboursement" >Retour et remboursement</a>
        </span>
            
        <!-- <img src="../assets/zalando-logo.png" alt=""> -->
        </div>
        <div class="mainHead">
            <div class="nav2">
            
                <div class="contenue" >
                <a  href="#femme">Femme</a>
                <a href="#homme">Homme</a>
                <a href="#enfant">Enfant</a>
               </div>
               <div class="contenue2">
                <img src="../assets/zalando-logo.png" alt="">
                <span>Découvrir</span>
                
               </div>
               <div class="contenue3">
                <a href="#"><img src="../assets/account.png" alt="Panier" ></a>
                <a href="#"><img src="../assets/whish.png" alt="Panier" ></a>
                <a href="#"><img src="../assets/bag.png" alt="Panier" ></a>
               </div>
               
            
        </div>




            <div class="nav">
            
                <nav>
                    <div class="dropdown" v-on:mouseenter="showDropdown(1)" v-on:mouseleave="hideDropdown(1)">
      <a href="#newin">New In</a>
      <Transition name="slide-fade">
        <div class="dropdown-menu" v-show="isDropdownVisible[1]" v-on:mouseenter="keepDropdown" v-on:mouseleave="hideDropdown(1)">
          <ul>
            <li v-on:mouseover="showDropdown(1)">Option 1</li>
            <li v-on:mouseover="showDropdown(1)">Option 2</li>
            <li v-on:mouseover="showDropdown(1)">Option 3</li>
          </ul>
        </div>
      </Transition>
    </div>

    <div class="dropdown" v-on:mouseenter="showDropdown(2)" v-on:mouseleave="hideDropdown(2)">
      <a href="#clothing">Vêtements</a>
      <Transition name="slide-fade">
        <div class="dropdown-menu" v-show="isDropdownVisible[2]" v-on:mouseenter="keepDropdown" v-on:mouseleave="hideDropdown(2)">
          <ul>
            <li v-on:mouseover="showDropdown(2)">Option 1</li>
            <li v-on:mouseover="showDropdown(2)">Option 2</li>
            <li v-on:mouseover="showDropdown(2)">Option 3</li>
          </ul>
        </div>
      </Transition>
    </div>
                    <a href="#shoes">Chaussures</a>
                    <a href="#accessories">Accessoires</a>
                    <a href="#streetwear">Streetwear</a>
                    <a href="#luxury">Luxe & Créateurs</a>
                    <a href="#sport">Sport</a>
                    <a href="#care">Soin</a>
                    <a href="#promos">Promos</a>
                    <a href="#inspirations">Inspirations</a>
                    
                        <input  type="text" placeholder="Rechercher">
                        
                    
                </nav>



                </div>
            </div>
        </div>

        

  </template>
    <script >




    import { ref } from 'vue'
    export default {
  setup() {
    const isDropdownVisible = ref({ 1: false, 2: false });

    const showDropdown = (dropdownNumber) => {
      isDropdownVisible.value[dropdownNumber] = true;
    };

    const hideDropdown = (dropdownNumber) => {
      isDropdownVisible.value[dropdownNumber] = false;
    };

    const keepDropdown = () => {
      // Optionnel : Ajoutez ici une logique spécifique si nécessaire
    };

    return {
      isDropdownVisible,
      showDropdown,
      hideDropdown,
      keepDropdown,
    };
  },
};
    
    //
    //
    
    </script>

<style lang="scss" >
@import url(https://db.onlinewebfonts.com/c/08e020de1811ec4489f82d1247a42c09?family=Helvetica+Now+Text);

.haut{
    padding: 8px 355px;
    padding-right: 540px;
    text-align: center;
    background: #efeff0;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
    align-items: center;

}
.haut a {
    font-family: "Helvetica Now Text";
    font-weight: bold;
    color: #666666;
    text-decoration: none;
    font-size: 12px;
    margin: 0;
}



.nav2{
    justify-content: space-between;
    overflow: hidden;
    display: flex;
    padding-top: 10px;
    
}
.contenue {
    padding-left: 355px;
    overflow: hidden;
    display: flex;
    font-weight: bold;
    font-size: 16px;
}

.contenue a{
    padding:6px 18px;
    background-color: black;
    color: white;
    text-decoration: none;
}
.contenue2 {
    padding-right: 0px;
    overflow: hidden;
    display: block;
    font-size: 16px;
}
.contenue2 img{
    width:130px;
}
.contenue2 span{
    padding:6px 18px;
    text-decoration: none;
    
    
    
}
.contenue3 {
    padding-right: 334px;
    overflow: hidden;
    display: block;
    
    
   
}
.contenue3 a  {
    padding:6px 7px;
}

nav {
    background-color: white;
    // overflow: hidden;
    text-align: center; /* Ajout de la propriété pour centrer horizontalement */
    // border-bottom: 1px solid;
    width: 100%;
    
}

/* Style des liens dans la barre de navigation */
nav a {
    display: inline-block; /* Ajustement pour permettre le centrage horizontal */
    color: black;
    text-align: center;
    padding: 12px 20px;
    text-decoration: none;
    font-size: 15px;
}

/* Style des liens au survol */
nav a:hover {
    text-decoration: underline;
    
}

.dropdown {
        position: relative;
        display: inline-block;
  
    }
    
    
    .dropdown-menu {
    position: absolute;
    top: 100%;
    left: 0;
    border: 1px solid #ccc;
    padding: 10px;
    width: 100% ;
}


.dropdown-menu ul a {
    text-decoration: none;
    color: black;
}


.dropdown-menu ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

.dropdown-menu li {
  padding: 8px;
  cursor: pointer;
}

.dropdown:hover .dropdown-menu,
.dropdown-menu:hover {
  display: block;
}


// transition

.slide-fade-enter-active {
  transition: opacity 0.3s ease-out, transform 0.3s cubic-bezier(0.25, 0.5, 0.75, 1.25);
}

.slide-fade-leave-active {
  transition: opacity 0.6s cubic-bezier(1, 0.5, 0.8, 1), transform 0.6s cubic-bezier(0.25, 0.5, 0.75, 1.25);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(20px);
  opacity: 0;
}



    
// }






/* Style de la barre de navigation */

.search-box {
    float: inline-end; /* Aligne la boîte de recherche à droite */
    margin-top: 10px; /* Ajuste la marge supérieure pour l'espacement */
    padding: 0px;
}

/* Style de l'input de recherche */
.search-box input {
    padding-left: 18px;
    margin-right: 15px;
}






</style>
