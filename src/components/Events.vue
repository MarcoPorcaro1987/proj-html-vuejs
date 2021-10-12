<template>
  <section class="events">
    <p class="special-color">Wanna transform your life?</p>
    <h2>Upcoming Events</h2>
    <div class="mid-container">
      <div class="events-cont" v-for="(event, index) in events" :key="index">
        <div class="event">
          <p class="special-color location">
            <i class="fas fa-map-marker-alt"></i> {{ event.location }}
          </p>
          <p class="event-title">{{ event.title }}</p>
        </div>
        <div class="event-date">
          <p class="special-color event-day">{{ event.day }}</p>
          <p class="event-month">{{ event.month }}</p>
          <div class="btn-common">Get ticket</div>
        </div>
      </div>
    </div>
    <p class="p-text">Excited about our event? <span class="special-color">View all events <i class="fas fa-long-arrow-alt-right"></i
          ></span></p>
  </section>
</template>

<script>
export default {
  name: "Events",
  data() {
    return {
      events: [
        {
          location: "Texas, US",
          title: "Storytelling Workshop",
          day: "22",
          month: "NOV",
        },
        {
          location: "New York, US",
          title: "Painting Art Contest 2000",
          day: "10",
          month: "OCT",
        },
        {
          location: "Hamburg, Germany",
          title: "Intenational Art Fair 2020",
          day: "23",
          month: "NOV",
        },
        {
          location: "Illinois, US",
          title: "Street Performance: Call for Artist",
          day: "15",
          month: "DEC",
        },
        {
          location: "Illinois, US",
          title: "Consumer Food Safety Education Conference",
          day: "22",
          month: "JUL",
        },
        {
          location: "Dubai",
          title: "How meditation improve your mental health?",
          day: "12",
          month: "AUG",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
.events {
  padding: 3.5rem 0;
  text-align: center;
  h2 {
    margin: 0.9375rem;
  }
  .mid-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1.25rem;
    .events-cont {
      width: calc(50% - 1.25rem);
      padding: 1.25rem;
      background-color: $bgColor;
      display: flex;
      justify-content: space-between;
      .event {
        text-align: left;
        width: 69%;
        .location {
          font-size: 0.75rem;
          margin-bottom: 0.625rem;
        }
        .event-title {
          color: $titleColor;
          font-weight: bold;
        }
      }
      .event-date {
        .event-day {
          font-size: 1.875rem;
        }
        .event-month {
          margin: 0.625rem 0;
          color: $titleColor;
          font-weight: bold;
        }
      }
    }
  }
  .p-text{
      margin-top: 1.875rem;
      span{
          font-weight: bold;
          border-bottom: .0625rem solid $secondaryColor;
      }
  }
}
</style>
