<template>
  <div class="relative">
    <div class="h-screen">
      <div class="flex flex-col">
        <!-- 
          Header Content ( Landing Page )

          PARAMETERS
          :imgURL (URL for Background)
          :header_txt ( Header Text )
          :second_header ( Header 2 Text)
          :descriptions ( Descriptions )
        -->
        <HeaderContent
          imgURL="data:image/jpeg;base64,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"
          header_txt="Adventure Company"
          second_header="Your journey begin here"
          descriptions="Hello world"
        ></HeaderContent>
        <!-- 
          About Content 

          PARAMETERS
          :imgURL ( URL for about us )
        -->
        <AboutContent
          imgURL="data:image/jpeg;base64,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"
        >
          <template v-slot:about>
            Welcome to [store name], your number one source for all things [product, ie: shoes, bags, dog treats]. We're dedicated to giving you the very best of [product], with a focus on [three characteristics, ie: dependability, customer service and uniqueness.]
            Founded in [year] by [founder's name], [store name] has come a long way from its beginnings in a [starting location, ie: home office, toolshed, Houston, TX.]. When [store founder] first started out, his/her passion for [passion of founder, ie: helping other parents be more eco-friendly, providing the best equipment for his fellow musicians] drove him to [action, ie: do intense research, quit her day job], and gave him the impetus to turn hard work and inspiration into to a booming online store. We now serve customers all over [place, ie: the US, the world, the Austin area], and are thrilled to be a part of the [adjective, ie: quirky, eco-friendly, fair trade] wing of the [industry type, ie: fashion, baked goods, watches] industry.
            We hope you enjoy our products as much as we enjoy offering them to you. If you have any questions or comments, please don't hesitate to contact us.
            Sincerely,
            Name, [title, ie: CEO, Founder, etc.]
          </template>
        </AboutContent>

        <ServiceContent>
          <template v-slot:services>
            <!-- 

              Service 

              PARAMETERS

              :imgURL (image url)
            -->
            <Service imgURL="/img/icon1.png" title="Service Title">
              <template
                v-slot:content
              >Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repellendus excepturi quisquam temporibus non nisi doloribus cumque cum molestiae odio velit ratione perspiciatis assumenda numquam quam porro, sed quasi quia possimus?</template>
            </Service>

            <Service imgURL="/img/icon2.png" title="Service Title">
              <template
                v-slot:content
              >Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repellendus excepturi quisquam temporibus non nisi doloribus cumque cum molestiae odio velit ratione perspiciatis assumenda numquam quam porro, sed quasi quia possimus?</template>
            </Service>

            <Service imgURL="/img/icon3.png" title="Service Title">
              <template
                v-slot:content
              >Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repellendus excepturi quisquam temporibus non nisi doloribus cumque cum molestiae odio velit ratione perspiciatis assumenda numquam quam porro, sed quasi quia possimus?</template>
            </Service>

            <Service imgURL="/img/icon4.png" title="Service Title">
              <template
                v-slot:content
              >Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repellendus excepturi quisquam temporibus non nisi doloribus cumque cum molestiae odio velit ratione perspiciatis assumenda numquam quam porro, sed quasi quia possimus?</template>
            </Service>
          </template>
        </ServiceContent>

        <!-- 
          Portfolio
        -->
        <PortfolioContent>
          <template v-slot:portfolio>
            <!-- 
              Project

              PARAMETERS
              :imgURL ( img URL for Project )
              :name ( Name of the Project )
              :project ( Name of Project Type)
              :projectURL ( Link Address to project)
            -->
            <Project
              imgURL="/img/about.jpg"
              name="Project Name"
              project="Project Type"
              projectURL="https://google.com"
            />
          </template>
        </PortfolioContent>
        <ContactContent
          address="Level 11, Menara KEN TTDI, No.37 Jalan Burhanuddin Helmi, Taman Tun Dr. Ismail"
          email="support@thelead.io"
          phone="6016-473 7281"
          imgURL="/img/lead-white-logo.png"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: "Adventure Company"
    };
  }
};
</script>