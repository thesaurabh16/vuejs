<template>
    <div>
        <pre>
            {{ JSON.stringify(formValues,null,2) }}
        </pre>
    </div>
<form @submit.prevent="submitForm">
    <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model.trim.lazy="formValues.name">
    </div>
    <div>
        <label for="profile">Profile Summary</label>
        <textarea id="profile" v-model="formValues.profileSummary" />
    </div>
    <div>
        <label for="country">Country</label>
        <select id="country" v-model="formValues.country">
            <option value="">select a country</option>
            <option value="Nepal">Nepal</option>
            <option value="India">India</option>
            <option value="china">China</option>

        </select>
    </div>
    <div>
        <label for="Job-location">Job Location</label>
        <select id="Job-location" multiple v-model="formValues.Joblocation">
            <option value="Nepal">Nepal</option>
            <option value="India">India</option>
            <option value="china">China</option>
        </select>
    </div>
    <div>
        <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no"/>
        <label for="remoteWork">Open to remove work?</label>
    </div>
    <div>
        <label >Skill Set</label>
        <input type="checkbox" id="html" value="html" v-model="formValues.skillSet"/>
        <label for="html">HTML</label>
        <input type="checkbox" id="css" value="css" v-model="formValues.skillSet" />
        <label for="css">CSS</label>
        <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet"/>
        <label for="javascript">Javascript</label>
    </div>
    <div>
        <label>Years of Experience</label>
        <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience"/>
        <label for="0-2">0-2</label>
        <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience"/>
        <label for="3-5">3-5</label>
        <input type="radio" id="6-9" value="6-9" v-model="formValues.yearsOfExperience"/>
        <label for="6-9">6-9</label>
        <input type="radio" id="9-12" value="9-12" v-model="formValues.yearsOfExperience"/>
        <label for="9-12">9-12</label>
    </div>
    <div>
        <label for="age">Age</label>
        <input @keyup.enter="submitForm" type="number" id="age" v-model.number="formValues.age" />
    </div>
    <!-- <div>
        <button>Submit</button>
    </div> -->
</form>
    
</template>
<script>
export default {
    name:'FormHandling',
    data(){
        return {
            formValues:{
                name:'',
                profileSummary:'',
                country:'',
                Joblocation:[],
                remoteWork:"no",
                skillSet:[],
                yearsOfExperience:[],
                age:null,
            },
        }
    },
    methods:{
        submitForm(){
            console.log('form Value',this.formValues)
        }
    },
}
</script>

<style scoped>
#FormHandling{
    font-family: Arial, Helvetica, sans-serif;
    -webkit-fonnt-smothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    /* text-align: center; */
    color: #2c3e50;
    margin-top: 60px;
}
label{
    font-weight: bold;
    display: flex;
    margin-bottom: 5px;
}
input + label{
    font-weight: bold;
    display: inline-flex;
    margin-right: 20px;
}
input[type='text'],
textarea,
select{
    display: block;
    width: 400px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.42857143;
    color: #555;
    background-color: #fff;
    background-image: none;
    border: 1px solid #ccc;
    border-radius: 4px;
}
</style>