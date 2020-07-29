<script>
  import { Collapse, Button, CardBody, Card } from 'sveltestrap'
  import { ArrowDownIcon, MapPinIcon } from 'svelte-feather-icons'

  import ButtonApply from 'components/Button/Button2.svelte'

  export let jobTitle = ''
  export let openPosition = 1
  export let location = ''
  export let jobCategory = 'IT and Software'
  export let jobLevel = 'Mid-Senior'
  export let educationLevel = "Bachelor's Degree Graduate"
  export let jobDescription = ''
  export let minimumQualification = ''

  let isOpen = false
</script>

<style>
  .job-opening-container {
    width: 100%;
    height: 100%;
    padding: 0px 20px 20px 0px;
    color: #444;
    position: relative;
    overflow: hidden;
  }

  .job-title-section {
    display: flex;
    height: 100%;
    justify-content: space-between;
    position: relative;
    align-items: center;
    cursor: pointer;
  }

  .job-title-intro,
  p {
    flex-wrap: wrap;
    margin: 0;
  }

  .job-txt-tilte {
    font-size: 24px;
    font-weight: 600;
    font-style: normal;
  }

  .job-txt-tilte:hover {
    color: #0082e6;
    cursor: pointer;
  }

  .job-location {
    display: flex;
    color: rgb(70, 71, 71);
    font-size: 18px;
    position: relative;
    align-items: center;
  }
  .jbLocation {
    margin-left: 10px;
    margin-right: 10px;
  }

  .job-details {
    display: flex;
    height: 100%;
    justify-content: space-between;
    position: relative;
    cursor: pointer;
    padding-top: 15px;
    margin-left: 20px;
    margin-right: 20px;
  }

  .job-description-row {
    margin-left: 20px;
    margin-right: 20px;
  }

  .btn-apply {
    text-align: right;
  }

  hr {
    background-color: #ccc;
    border: 0;
    height: 1px;
  }
</style>

<div class="job-opening-container" on:click={() => (isOpen = !isOpen)}>
  <div class="job-title-section">
    <div class="job-title-intro">
      <h1 class="job-txt-tilte">{jobTitle}</h1>
      <p>{openPosition} opening(s)</p>
    </div>
    <div class="job-location">
      <MapPinIcon size="20" class="jbLocation" />
      <p class="jbLocation">{location}</p>
      <ArrowDownIcon size="20" class="jbLocation" />
    </div>
  </div>
  <hr />

  <Collapse {isOpen}>

    <div class="job-openings-collapse">

      <div class="job-details">
        <div class="job-category">
          <strong>
            <p>Job Category:</p>
          </strong>
          <p>{jobCategory}</p>
        </div>
        <div class="job-level">
          <strong>
            <p>Job Level:</p>
          </strong>
          <p>{jobLevel}</p>
        </div>
        <div class="job-education">
          <strong>
            <p>Educational Attainment:</p>
          </strong>
          <p>{educationLevel}</p>
        </div>

      </div>

      <hr />
      <div class="job-description">
        <div class="job-description-row">
          <h1 class="job-txt-tilte">Job Description</h1>
          <ul>
            {#each jobDescription as description}
              <li>{description}</li>
            {/each}
          </ul>

          <h1 class="job-txt-tilte">Minimum Qualifications</h1>
          <ul>
            {#each minimumQualification as qualifacation}
              <li>{qualifacation}</li>
            {/each}
          </ul>
        </div>
        <div class="btn-apply">
          <ButtonApply name="APPLY NOW" />
        </div>
      </div>
    </div>
  </Collapse>
</div>
