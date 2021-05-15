<template>
  <footer>
    <div class="links-footer">
      <ul>
        <li v-for="link in company" :key="link">{{ link }}</li>
      </ul>
      <ul>
        <li v-for="link in products" :key="link">{{ link }}</li>
      </ul>
      <ul>
        <li v-for="link in community" :key="link">{{ link }}</li>
      </ul>
      <ul>
        <li v-for="link in solutions" :key="link">{{ link }}</li>
      </ul>
      <ul>
        <li v-for="link in contact" :key="link">{{ link }}</li>
      </ul>
    </div>

    <div class="bottom-footer">
      <div class="left-side container">
        <img
          src="https://www-static.cdn.prismic.io/www-static%2F903fd83b-8963-42c2-baf6-44f4d6bb83f2_digitalocean-logo-mark.svg"
          alt=""
        />
        <p>© 2021 DigitalOcean, LLC. All rights reserved.</p>
      </div>

      <div class="right-side container">
        <!-- Icons -->
      <ul class="icons-container">
        <li v-for="icon in icons" :key="icon">
          <i :class="icon "></i>
        </li>
      </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    msg: String
  },
    data() {
    return {
      company: [
        "Company",
        "About",
        "Leadership",
        "Blog",
        "Careers",
        "Partners",
        "Referral Program",
        "Press",
        "Legal",
        "Trust Platform",
        "Investor Relations",
      ],
      products: [
          "Products",
          "Products Overview",  
          "Droplets",
          "Kubernetes",
          "Managed Databases",
          "Spaces",
          "Marketplace",
          "Load Balancers",
          "Block Storage",
          "Tools & Integrations",
          "API",
          "Pricing",
          "Documentation",
          "Release Notes"
      ],
      community: [
          "Community",
          "Tutorials",  
          "Meetups",
          "Q&A",
          "Write for Donations",
          "Droplets for Demos",
          "Hatch Startup Program",
          "Shop Swag",
          "Research Program",
          "Currents Research",
          "Open Source",
          "Code of Conduct"
      ],
      solutions: [
          "Solutions",
          "Web & Mobile Apps",  
          "Website Hosting",
          "Streaming",
          "VPN",
          "Startups",
          "SaaS Solutions",
          "Agency & Web Dev Shops",
          "Managed Cloud Hosting Providers",
          "Big Data",
          "Business Solutions"
      ],
      contact: [
          "Contact",
          "Support",  
          "Sales",
          "Report Abuse",
          "System Status"
      ],
      icons: [
        "fab fa-twitter",
        "fab fa-facebook-square",
        "fab fa-instagram",
        "fab fa-youtube",
        "fab fa-linkedin",
        "fab fa-dev"
      ]


    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
    background-color: hsl(220,95%,8%);
    color: hsla(0,0%,100%,0.5);
    justify-content: center;
}



.links-footer {
  display: flex;
  justify-content: center;
  text-align: left;
  padding-top: 95px;
}

.links-footer ul li:first-child {
  font-weight: 500;
  color: white;
  margin-bottom: 20px;
  pointer-events: none;
}

.links-footer ul li:last-child {
  margin-bottom: 40px;
}

.bottom-footer {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  max-width: 1100px;
  margin:  30px auto;
  padding: 0 20px 30px 20px;
  border-top: 1px solid hsla(0,0%,100%,0.5);;
  padding-top: 30px;
}

.left-side {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.left-side img {
  margin: 10px 30px 10px 30px;
}

ul {
  width: 170px;
}

ul > li {
  list-style: none;
  margin-bottom: 10px;
  font-size: 14px;
  cursor: pointer;
}

ul > li:hover {
  text-decoration: underline;
}

.icons-container {
  display: flex;
  padding-right: 20px;
}

i {
  font-size: 21px;
  margin-right: 30px;
}


@media screen and (max-width: 768px) {

  .links-footer {
    min-height: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
  }
  ul {
    width: 35%;
  }

  .bottom-footer {
    flex-direction: column;
  }

  p {
    text-align: center;
  }

  .icons-container{
    justify-content: flex-start;
    width: 100%;
    margin-top: 15px;
  }

  i {
    margin-right: 40px;
  }

}

</style>