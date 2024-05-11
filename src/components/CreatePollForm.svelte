
<script>
    import Button from "../shared/Button.svelte";
let fields ={
    question:'',
    answerA:'',
    answerB:''
}
const handleSubmit = () =>{

}
</script>


<form on:submit|preventDefault={handleSubmit}>
    <div class="form-field">
        <label for="question">Poll Question</label>
        <input type="text" bind:value={fields.question}  id="question">
    </div>

    <div class="form-field">
        <label for="answer-a">Answer A:</label>
        <input type="text" bind:value={fields.answerA}  id="answer-a">
    </div>

    <div class="form-field">
        <label for="answer-b">Answer B:</label>
        <input type="text" bind:value={fields.answerB} id="answer-b">
    </div>

    <Button type='secondary' flat={true}>
        Add Poll
    </Button>
</form>


<style>

form{
    width: 400px;
    margin: 0 auto;
    text-align: center;
}

.form-field{
    margin: 18px auto;
}

input{
    width: 100%;
    border-radius: 6px;
}

label{
    margin: 10px auto;
    text-align: left;
}
</style>