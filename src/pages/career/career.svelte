<script>
  import CardContent from 'components/CardContent/card-content.svelte'
  import JobOpening from '../career/components/job-opening.svelte'
  import ApplyForm from './components/apply-form.svelte'
  import jobs from 'vars/jobs.json'

  $: datas = jobs.data

  console.log(jobs.data)
</script>

<style>
  .stark-career {
    margin: 0;
    position: relative;
    width: 100vw;
  }

  .content-container {
    width: 100%;
    height: 200px;
  }

  .career-header {
    width: 100%;
    height: 100%;
    padding-bottom: 50px;
  }

  .join-the-team {
    padding-top: 20px;
    padding-bottom: 50px;
    width: 100%;
    align-items: center;
    position: relative;
    display: flex;
    justify-content: center;
  }

  .join-the-team h1 {
    font-size: 35;
    font-weight: bold;
    color: #474646;
  }

  .join-section {
    width: 76%;
  }

  .apply-label {
    margin-top: 50px;
    height: 100px;
    color: #474646;
    font-size: 25px;
    text-align: center;
    font-weight: bold;
  }
</style>

<div class="stark-career">
  <div class="career-header">
    <CardContent src="images/job.png" name={'Join our team!'} />
  </div>

  <div class="join-the-team">
    <div class="join-section">
      <div>
        <h1>Life at Stark Technologies</h1>
      </div>
      <div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
      </div>
    </div>
  </div>

  <div class="join-the-team">
    <div class="join-section">
      {#each datas as data (data.id)}
        <JobOpening
          jobTitle={data.position}
          location={data.location}
          openPosition={data.openPosition}
          jobCategory={data.category}
          jobLevel={data.level}
          educationLevel={data.education}
          jobDescription={data.jobDescription}
          minimumQualification={data.minimumQualifications} />
      {/each}
      <div class="apply-section">
        <div class="apply-label">
          Be part of our Stark Technologies Community. Apply now.
        </div>
        <ApplyForm />
      </div>
      <div class="content-container" />
    </div>
  </div>

</div>
