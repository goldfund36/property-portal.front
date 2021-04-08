<template>
  <div class="container">
    <div class="row">
      <div class="property-block all mix sale col-lg-4 col-md-6 col-sm-12" v-for="i of 18" style="display: inline-block;">
        <div class="inner-box">
          <div class="image-box">
            <figure class="image"><img src="/images/estate1.jpg" alt=""></figure>
            <span class="for">FOR SALE</span>
            <span class="featured">FEATURED</span>
            <ul class="info clearfix">
              <li><i class="la la-calendar-minus-o"></i>2 Years Ago</li>
            </ul>
          </div>
          <div class="lower-content">
            <ul class="tags">
              <li><a href="/">Apartment</a>,</li>
              <li><a href="/">Modern Villa</a></li>
            </ul>
            <h3><a href="/">Modern Apartment in City Center</a></h3>
            <div class="lucation"><i class="la la-map-marker"></i> 121, King St, VIC 3000, New York, United States</div>
            <ul class="property-info clearfix">
              <li><i class="flaticon-money"></i>$ 1,51,000</li>
              <li><i class="flaticon-bed"></i> 4 Bedrooms</li>
              <li><i class="flaticon-car"></i> 2 Garage</li>
              <li><i class="flaticon-bathtub"></i> 3 Bathroom</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "PropertyCard"
}
</script>

<style>
.property-block {
  position: relative;
  margin-bottom: 60px;
}
.property-block .inner-box {
  position: relative;
}
.property-block .image-box {
  position: relative;
  overflow: hidden;
}
.property-block .image-box .image {
  position: relative;
  margin: 0;
}
.property-block .image-box .image:before {
  position: absolute;
  left: 0;
  bottom: 0;
  height: 40%;
  width: 100%;
  background: -moz-linear-gradient(top, rgba(34,34,34,0) 0%, rgba(34,34,34,0.99) 99%, rgba(34,34,34,1) 100%);
  background: -webkit-linear-gradient(top, rgba(34,34,34,0) 0%,rgba(34,34,34,0.99) 99%,rgba(34,34,34,1) 100%);
  background: linear-gradient(to bottom, rgba(34,34,34,0) 0%,rgba(34,34,34,0.99) 99%,rgba(34,34,34,1) 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00222222', endColorstr='#222222',GradientType=0 );
  content: "";
  z-index: 99;
}
.property-block .image-box .image img {
  display: block;
  width: 100%;
  max-width: 100%;
  height: auto;
  -webkit-transition: all 00ms ease;
  -moz-transition: all 400ms ease;
  -ms-transition: all 400ms ease;
  -o-transition: all 400ms ease;
  transition: all 400ms ease;
}
.property-block .image-box .for {
  position: absolute;
  left: 15px;
  top: 25px;
  font-size: 13px;
  line-height: 23px;
  color: #ffffff;
  font-weight: 700;
  background-color: #00a75e;
  padding: 0 18px;
  text-align: center;
  z-index: 9;
  border-radius: 5%;
}
.property-block .image-box .featured {
  position: absolute;
  right: 0;
  top: 25px;
  font-size: 13px;
  line-height: 23px;
  color: #ffffff;
  font-weight: 700;
  text-transform: uppercase;
  padding: 0 7px;
  z-index: 9;
  background-color: #00a75e;
}
.property-block-two h3 a:hover, .property-block-two .property-info li i, .time-counter .time-countdown .counter-column, .property-block-two .lucation i, .property-block-two .tags li a, .blog-detail .post-share-options .social-icon li a:hover, .header-style-seven .main-menu .navigation > li:hover > a, .header-style-seven .main-menu .navigation > li.current > a, .header-style-three .main-menu .navigation > li:hover > a, .header-style-three .main-menu .navigation > li.current > a, .new-property h3 a:hover, .header-style-six .main-menu .navigation > li:hover > a, .header-style-six .main-menu .navigation > li.current > a, .recent-properties .post:hover h3 a, .recent-properties .post .location, .cat-list li.active a, .cat-list li:hover a, .service-block .icon-box, .popular-posts .post h4 a:hover, .agent-widget .social-links li a, .agent-widget .social-links li, .agent-widget .info-box .designation, .main-footer .footer-bottom .footer-nav ul li a:hover, .main-footer .list li a:hover, .main-footer .list li:before, .main-footer .contact-list li a:hover, .main-footer .contact-list li span, .social-icon-two li a:hover, .accordion-box .block .icon, .accordion-box .block .acc-btn.active, .testimonial-carousel-two .owl-next:hover, .testimonial-carousel-two .owl-prev:hover, .testimonial-block-two .info-box .name, .testimonial-block .content-box .rating span, .testimonial-block .content-box .name, .blog-detail .post-share-options .tags a:hover, .blog-detail .lower-content .info li span, .news-block-three .content-box h3 a:hover, .news-block-three .content-box .info li span, .news-block-two .content-box .info li i, .news-block-two .content-box h4 a:hover, .news-block .lower-content h3 a:hover, .news-block .lower-content .info li span, .process-block h4 a, .feature-block-two h4 a:hover, .feature-block-two .inner-box:hover .icon-box, .agent-detail .contact-info .social-links li a i, .agent-detail .contact-info ul li span, .agent-detail .contact-info ul li a:hover, .agent-detail .contact-info ul li i, .agent-detail .designation, .agent-block .info-box .name a, .agent-block .info-box .name, .service-block .link-box a, .service-block h4 a:hover, .sec-title .title, .btn-style-six, .popular-places-carousel .owl-next:hover, .popular-places-carousel .owl-prev:hover, .popular-item-two .info-box .category a:hover, .about-us.style-two .feature-block h4 a:hover, .feature-block h4 a:hover, .feature-block .inner-box .icon, .fun-facts-section .column .icon-box, .lucation-info-box .info-box .price span, .lucation-info-box .info-box .othre-options li a:hover, .property-block-four .property-info li i, .property-block-four .location i, .property-block-four .price i, .property-block-four h3 a:hover, .property-block-three .property-info li i, .property-block-three .lucation i, .property-block-three h3 a:hover, .property-block-three .tags li a, .property-block-three .tags li, .property-block-three .image-box .info li a:hover, .property-block-three .image-box .info li i, .sidebar-page-container .filter-options li.active a, .sidebar-page-container .filter-options li a:hover, .property-filter-section .mixitup-gallery .filters li.active, .property-filter-section .mixitup-gallery .filters li:hover, .review-area .review-box .rating a:hover, .review-area .review-box .rating, .review-area .review-box .date i, .flooring-tabs .tab-buttons li:hover, .flooring-tabs .tab-buttons li.active-btn, .property-detail .thumbs-carousel .owl-prev:hover, .property-detail .thumbs-carousel .owl-next:hover, .upper-info-box .price-column .price, .upper-info-box .property-info li i, .upper-info-box .location i, .property-block-two .tags li, .property-block-two .image-box .info li a:hover, .property-block-two .image-box .info li i, .property-carousel .owl-next:hover, .property-carousel .owl-prev:hover, .new-property .property-info li i, .new-property .lucation i, .property-block .property-info li i, .property-block .lucation i, .property-block h3 a:hover, .property-block .tags li a, .property-block .tags li, .property-block .image-box .info li a:hover, .property-block .image-box .info li i, .property-search-section-two .content-box h2 span, .property-search-form .range-slider-one .theme-btn:hover, .banner-carousel .content-box .price, .banner-carousel .content-box .info-box li span, .main-slider .info-list li span, .page-title .bread-crumb li a, .header-style-seven .info-box .icon-box, .header-style-seven .top-right ul li a:hover, .header-style-seven .top-left .text span, .header-style-six .outer-box .social-icon-one li a:hover, .header-style-six .outer-box .link-box a:hover, .header-style-four .main-menu .navigation > li.current > a, .header-style-four .main-menu .navigation > li:hover > a, .header-style-four .main-menu .navigation > li:before, .header-style-three .info-box .icon-box, .header-style-three .top-right ul li a:hover, .header-style-three .top-left .text span, .main-menu .navigation > li.current > a, .main-menu .navigation > li:hover > a, .social-icon-one li a:hover, .main-header .top-left .contact-list li a:hover, .main-header .top-left .contact-list li i, .scroll-to-top:hover, .banner-section.style-two .content-box h2 span, .sticky-header .main-menu .navigation > li:hover > a, .sticky-header .main-menu .navigation > li.current > a, .sticky-header .main-menu .navigation > li.current-menu-item > a, .list-style-one li:before, .btn-style-four:hover, .btn-style-three:hover, .theme_color, .testimonial-block .content-box .icon, a {
  color: #00a75e;
}

.property-block .image-box .featured:before {
  position: absolute;
  left: -10px;
  top: 0;
  width: 0;
  height: 0;
  border-top: 20px solid #00a75e;
  border-left: 10px solid transparent;
  content: "";
  -webkit-transition: all 300ms ease;
  -moz-transition: all 300ms ease;
  -ms-transition: all 300ms ease;
  -o-transition: all 300ms ease;
  transition: all 300ms ease;
}
.property-block .image-box .info {
  position: absolute;
  bottom: 20px;
  width: 100%;
  padding: 0 20px;
  z-index: 99;
}
.property-block .image-box .info li:last-child {
  float: right;
  margin-right: 0;
}
.property-block .image-box .info li {
  position: relative;
  float: left;
  font-size: 12px;
  line-height: 15px;
  color: #ffffff;
  font-weight: 400;
  margin-right: 20px;
  z-index: 9;
}
.property-block .image-box .info li:first-child {
  float: left;
}
ul, li {
  list-style: none;
  padding: 0px;
  margin: 0px;
}
.clearfix::after {
  display: block;
  clear: both;
  content: "";
}
.property-block .lower-content {
  position: relative;
  padding: 20px 0 0;
}
.property-block .tags {
  position: relative;
  margin-bottom: 7px;
}
ul, li {
  list-style: none;
  padding: 0px;
  margin: 0px;
}
.property-block .tags li {
  position: relative;
  display: inline-block;
  font-size: 14px;
  line-height: 24px;
  color: #00a75e;
  font-weight: 400;
}
.property-block .tags li a:hover {
  color: #222222;
  text-decoration: none;
}
.property-block h3 {
  position: relative;
  display: block;
  font-size: 22px;
  line-height: 1.2em;
  color: #222222;
  font-weight: 700;
  margin-bottom: 7px;
}
.property-block h3 a {
  color: #222222;
  text-decoration: none;
  -webkit-transition: all 300ms ease;
  -moz-transition: all 300ms ease;
  -ms-transition: all 300ms ease;
  -o-transition: all 300ms ease;
  transition: all 300ms ease;
}
.property-block .lucation {
  position: relative;
  display: block;
  font-size: 14px;
  line-height: 24px;
  color: #777777;
  font-weight: 400;
  margin-bottom: 18px;
}
.property-block .property-info {
  position: relative;
  margin-bottom: 30px;
}
.property-block .property-info li {
  position: relative;
  float: left;
  width: 50%;
  padding-left: 45px;
  font-size: 16px;
  line-height: 45px;
  color: #777777;
  cursor: default;
  font-weight: 400;
}
.property-block .property-info li i {
  position: absolute;
  left: 0;
  top: 0;
  font-size: 24px;
  color: #00a75e;
  line-height: 40px;
}
.property-block .lucation i {
  font-size: 18px;
  margin-right: 4px;
}
</style>
