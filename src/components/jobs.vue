<template>
  <div class="container">
    <div
      v-for="(job, index) in jobs"
      :key="index"
      class="job-card d-flex align-items-center mb-3"
    >
      <div class="job-logo-container">
        <img :src="job.logoUrl" alt="Logo empresa" class="rounded job-logo" />
      </div>
      <div class="job-content">
        <h2 class="job-title bold">{{ job.name }}</h2>
        <div class="job-details">
          <div class="detail text-truncate text-capitalize">
            <font-awesome-icon icon="building" /> {{ job.company }}
          </div>
          <div class="detail text-truncate">
            <font-awesome-icon icon="briefcase" /> {{ job.type }}
          </div>
          <div class="detail text-truncate">
            <font-awesome-icon icon="dollar-sign" /> {{ job.salary }}
          </div>
          <div class="detail">
            <font-awesome-icon icon="users" /> Vacante: {{ job.vacancies }}
          </div>
          <div class="detail">
            <font-awesome-icon icon="clock" /> {{ job.timePosted }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "JobListings",
  data() {
    return {
      jobs: [
        {
          name: "Backend Developer",
          company: "Tech Corp",
          type: "Remoto",
          salary: "2.5 M COP",
          vacancies: 2,
          timePosted: "Hace 1 día",
          logoUrl: require("@/assets/img1.png"),
        },
        {
          name: "Frontend Developer",
          company: "Web Solutions",
          type: "Presencial",
          salary: "2.2 M COP",
          vacancies: 3,
          timePosted: "Hace 2 días",
          logoUrl: require("@/assets/img2.png"),
        },
        {
          name: "Full Stack Developer",
          company: "Innovative Startups",
          type: "Híbrido",
          salary: "3.0 M COP",
          vacancies: 1,
          timePosted: "Hace 3 días",
          logoUrl: require("@/assets/img3.png"),
        },
        {
          name: "Data Scientist",
          company: "DataWise Analytics",
          type: "Remoto",
          salary: "3.5 M COP",
          vacancies: 2,
          timePosted: "Hace 1 semana",
          logoUrl: require("@/assets/img4.png"),
        },
        {
          name: "DevOps Engineer",
          company: "CloudTech Solutions",
          type: "Presencial",
          salary: "3.2 M COP",
          vacancies: 1,
          timePosted: "Hace 5 días",
          logoUrl: require("@/assets/img5.png"),
        },
        {
          name: "UI/UX Designer",
          company: "Creative Design Studio",
          type: "Híbrido",
          salary: "2.0 M COP",
          vacancies: 2,
          timePosted: "Hace 2 semanas",
          logoUrl: require("@/assets/img6.png"),
        },
        {
          name: "Developer",
          company: "Tech.co",
          type: "Remoto",
          salary: "5.5 M COP",
          vacancies: 5,
          timePosted: "Hace 4 día",
          logoUrl: require("@/assets/img1.png"),
        },
        {
          name: "Developer Java",
          company: "Solutions Tech",
          type: "Presencial",
          salary: "4.2 M COP",
          vacancies: 7,
          timePosted: "Hace 7 días",
          logoUrl: require("@/assets/img2.png"),
        },
        {
          name: "Full Stack Developer JS, Java, Python",
          company: "Startups",
          type: "Híbrido",
          salary: "7.0 M COP",
          vacancies: 3,
          timePosted: "Hace 14 días",
          logoUrl: require("@/assets/img3.png"),
        },
        {
          name: "Data Scientist",
          company: "Analytics Up",
          type: "Remoto",
          salary: "6.5 M COP",
          vacancies: 3,
          timePosted: "Hace 2 semanas",
          logoUrl: require("@/assets/img4.png"),
        },
        {
          name: "DevOps",
          company: "CloudTech Corp",
          type: "Presencial",
          salary: "3.7 M COP",
          vacancies: 2,
          timePosted: "Hace 6 días",
          logoUrl: require("@/assets/img5.png"),
        },
        {
          name: "UI/UX Designer",
          company: "Studio 77",
          type: "Híbrido",
          salary: "3.0 M COP",
          vacancies: 3,
          timePosted: "Hace 4 semanas",
          logoUrl: require("@/assets/img6.png"),
        }
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.job-card {
  width: 95%;
  border: 1px solid gainsboro;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 15px;
  display: flex;
  align-items: flex-start;
  margin-top: 20px;
  border-radius: 5px;
}

.job-card:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.job-logo-container {
  margin-right: 15px;
}

.job-logo {
  width: 70px;
  height: 70px;
}

.job-content {
  display: flex;
  flex-direction: column;
  margin-left: 20px;
}

.job-title {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 10px;
  margin-top: 0;
  text-align: left;
}

.job-details {
  font-size: 0.9rem;
  display: flex;
  flex-wrap: wrap;
}

.detail {
  margin-right: 140px;
  margin-bottom: 5px;
}
</style>
