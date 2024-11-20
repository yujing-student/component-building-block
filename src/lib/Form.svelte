<script>
    import TextButton from '$lib/Subscribe.svelte'


</script>
<h1>INSCHRIJVEN</h1>


<form >
    <fieldset>
        <legend>persoonlijke gegevens</legend>
        <label for="functie" class="form-label" >
            Functie*
            <!--            <span class="star">*</span>-->
            <input id="functie" class="Mandatory" type="text" placeholder="" required aria-required="true"/>
        </label>
        <label for="Voornaam" class="form-label" >Voornaam*
            <!--            <span class="star">*</span>-->
            <input id="Voornaam" class="Mandatory" type="text" placeholder="" required aria-required="true"
            />
        </label>
        <label for="Tussenvoegsel" class="form-label" >
            Tussenvoegsel
            <input id="Tussenvoegsel" type="text" placeholder=""/>
        </label>
        <label for="Achternaam" class="form-label" >
            Achternaam*
            <!--            <span class="star">*</span>-->
            <input id="Achternaam" class="Mandatory" placeholder="" type="text" required aria-required="true"/>
        </label>

        <label for="email" class="form-label"  >
            E-mail*
            <!--            <span class="star">*</span>-->
            <input id="email"  class="Mandatory" placeholder="Enter email..." type="email"/>

        </label>
        <label for="Mobiel" class="form-label" >
            Mobiel*
            <!--            <span class="star">*</span>-->
            <input id="Mobiel"  type="tel" placeholder="" class="Mandatory"
                   required
                   aria-required="true"/>
        </label>
        <label for="Bedrijfsnaam" class="form-label" >
            Bedrijfsnaam*
            <!--            <span class="star">*</span>-->
            <input id="Bedrijfsnaam" class="Mandatory" placeholder="" type="text" required aria-required="true"/>
        </label>
        <label for="Bedrijfswebsite" class="form-label ">
            Bedrijfswebsite*
            <!--            <span class="star">*</span>-->
            <input id="Bedrijfswebsite"  class="Mandatory" placeholder="" type="text" required aria-required="true" />
        </label>


        <label for="ik-wil-graag-lid-worden-omdat" class="form-label input-textfield" >
            Ik wil graag lid worden omdat*
            <!--            <span class="star">*</span>-->
            <textarea id="ik-wil-graag-lid-worden-omdat" placeholder="" class="Mandatory" required aria-required="true">

            </textarea>
        </label>
        <label for="FTE" class="dropown">
            FTE*
            <!--            <span class="star">*</span>-->
            <select id="FTE" required aria-required="true"  placeholder="" class="Mandatory">
                <option value="1-9">
                    1-9
                </option>
                <option value="10-24">
                    10-24
                </option>
                <option value="25-49">
                    25-49
                </option>
                <option value="50-99">
                    50-99
                </option>
                <option value="100-249">
                    100-249
                </option>
                <option value="250+">
                    250
                </option>
            </select>
        </label>

        <TextButton/>
    </fieldset>
</form>

<style>
    form{
        color: var(--grey);
    }
    fieldset{
        border: none;
    }
    legend{
        position: absolute;
        top: 0;
        left: -9999px;
    }
    textarea{
        height: auto;
    }
    input,textarea, select{

        border: none;
    }
    label {
        margin-top: 1.8rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 100%;
        border-bottom: 1.5px solid var(--black);
        gap: 0.8rem;
    }


    /*ui states*/
    /*.Mandatory:invalid {*/
    /*    border-bottom: 1.5px solid red;*/
    /*}*/

    /*.Mandatory:valid {*/
    /*    border-bottom: 1.5px solid green;*/
    /*}*/

    /*input::placeholder{*/
    /*    color: var(--blue);*/
    /*}*/

    /*input[type='email']:invalid{*/
    /*    border-bottom: 1.5px solid red;*/
    /*}*/
    input:focus{
        outline: 2px solid var(--blue);
    }
    textarea:focus{
        outline: 2px solid var(--blue);
    }
    /*textarea:invalid{*/
    /*    outline: 2px solid red;*/
    /*}*/


    input:invalid:not(:placeholder-shown) {
        border-bottom: 1px solid red;
    }

    input:invalid:not(:placeholder-shown) + p {
        color: red;
    }
    /*input [type="email"]:valid {*/
    /*    border: 1px solid green;*/
    /*}*/

    input:valid{
        border-bottom: green 1px solid;
    }

    input:invalid ~ button[type="submit"] {
        pointer-events: none;
        opacity: 0.7;
    }






    input:invalid ~ button[type="submit"] {
        pointer-events: none;
        opacity: 0.7;
    }

    /*https://codepen.io/adhikareeprayush/details/vYoYPXV*/
    /*bron sourche code*/

    /*@media (max-width: 700px) {*/
    /*    .form-label {*/
    /*        margin-top: 1.8rem;*/
    /*        display: flex;*/
    /*        flex-direction: column;*/
    /*        justify-content: center;*/
    /*        width: 100%;*/
    /*        border-bottom: 1.5px solid var(--black);*/
    /*    }*/
    /*}*/

    /*@media (min-width: 800px) {*/
    /*    fieldset {*/
    /*        display: grid;*/
    /*        grid-template-columns: auto auto;*/
    /*        !*background-color: red;*!*/
    /*        max-width: 700px;*/
    /*        gap: 1rem;*/
    /*    }*/
    /*    .input-textfield{*/
    /*        grid-row: 6;*/
    /*        grid-column-start: 1;*/
    /*        grid-column-end: 3;*/
    /*    }*/
    /*    .dropown{*/
    /*        grid-row: 7;*/
    /*    }*/
    /*}*/


    /*todo dit moet een fieldset worden met 2 rijen*/
    .form-label {
        container-name: main;
        container-type: inline-size;
    }
    @container main (max-width: 700px) {
        .form-label {
            margin-top: 1.8rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            width: 100%;
            border-bottom: 1.5px solid black;
        }
    }

    @container main (min-width: 700px) {
        .form-label {
           display: grid;
            grid-template-columns: auto auto;
            background-color: red;

        }
    }


    @container main (min-width: 1100px) {
        .form-label {
            margin-top: 1.8rem;
            display: grid;
            grid-template-columns: auto auto;
            justify-content: center;
            width: 100%;
            border-bottom: 1.5px solid black;
        }
    }

</style>


