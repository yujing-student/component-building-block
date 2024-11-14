
<script>
    import TextButton from '$lib/Subscribe.svelte'
</script>
<h1>inschrijven</h1>


<form>
    <fieldset>
        <legend>persoonlijke gegevens</legend>
        <label for="functie" class="form-label" >
            Functie*
            <!--            <span class="star">*</span>-->
            <input id="functie" type="text" required aria-required="true"/>
        </label>
        <label for="Voornaam" class="form-label" >Voornaam*
            <!--            <span class="star">*</span>-->
            <input id="Voornaam"  type="text" required aria-required="true"
            />
        </label>
        <label for="Tussenvoegsel" class="form-label" >
            Tussenvoegsel
            <input id="Tussenvoegsel" type="text"/>
        </label>
        <label for="Achternaam" class="form-label" >
            Achternaam*
            <!--            <span class="star">*</span>-->
            <input id="Achternaam"  type="text" required aria-required="true"/>
        </label>

        <label for="email" class="form-label"  >
            E-mail*
            <!--            <span class="star">*</span>-->
            <input id="email" type="email"/>
        </label>
        <label for="Mobiel" class="form-label" >
            Mobiel*
            <!--            <span class="star">*</span>-->
            <input id="Mobiel"  type="tel" required aria-required="true"/>
        </label>
        <label for="Bedrijfsnaam" class="form-label" >
            Bedrijfsnaam*
            <!--            <span class="star">*</span>-->
            <input id="Bedrijfsnaam"  type="text" required aria-required="true"/>
        </label>
        <label for="Bedrijfswebsite" class="form-label ">
            Bedrijfswebsite*
            <!--            <span class="star">*</span>-->
            <input id="Bedrijfswebsite"    type="text" required aria-required="true" />
        </label>


        <label for="ik-wil-graag-lid-worden-omdat" class="form-label input-textfield" >
            ik wil graag lid worden omdat*
            <!--            <span class="star">*</span>-->
            <textarea id="ik-wil-graag-lid-worden-omdat" required aria-required="true">

            </textarea>
        </label>
        <label for="FTE" class="dropown">
            FTE*
            <!--            <span class="star">*</span>-->
            <select id="FTE" required aria-required="true" >
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
        color: #666666;
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
        border-bottom: 1.5px solid black;
        gap: 0.8rem;
    }




    @media (max-width: 700px) {
        .form-label {
            margin-top: 1.8rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            width: 100%;
            border-bottom: 1.5px solid black;
        }
    }

    @media (min-width: 800px) {
        fieldset {
            display: grid;
            grid-template-columns: auto auto;
            /*background-color: red;*/
            max-width: 700px;
            gap: 1rem;
        }
        .input-textfield{
            grid-row: 6;
            grid-column-start: 1;
            grid-column-end: 3;
        }
        .dropown{
            grid-row: 7;
        }
    }

    /*.form-label {*/
    /*    container-name: main;*/
    /*    container-type: inline-size;*/
    /*}*/
    /*@container main (max-width: 700px) {*/
    /*    .form-label {*/
    /*        margin-top: 1.8rem;*/
    /*        display: flex;*/
    /*        flex-direction: column;*/
    /*        justify-content: center;*/
    /*        width: 100%;*/
    /*        border-bottom: 1.5px solid black;*/
    /*    }*/
    /*}*/

    /*@container main (min-width: 700px) {*/
    /*    .form-label {*/
    /*       display: grid;*/
    /*        grid-template-columns: auto auto;*/
    /*        background-color: red;*/

    /*    }*/
    /*}*/
</style>





<!--<script>-->
<!--    import TextButton from '$lib/Subscribe.svelte'-->
<!--</script>-->

<!--<style>-->

<!--    form{-->
<!--        color: #666666;-->
<!--    }-->
<!--    fieldset{-->
<!--        border: none;-->
<!--    }-->
<!--    legend{-->
<!--        position: absolute;-->
<!--        top: 0;-->
<!--        left: -9999px;-->
<!--    }-->
<!--    textarea{-->
<!--        height: auto;-->
<!--    }-->
<!--    input,textarea, select{-->

<!--        border: none;-->
<!--    }-->
<!--    label {-->
<!--        margin-top: 1.8rem;-->
<!--        display: flex;-->
<!--        flex-direction: column;-->
<!--        justify-content: center;-->
<!--        width: 100%;-->
<!--        border-bottom: 1.5px solid black;-->
<!--    }-->




<!--    @media (max-width: 700px) {-->
<!--            .form-label {-->
<!--                margin-top: 1.8rem;-->
<!--                display: flex;-->
<!--                flex-direction: column;-->
<!--                justify-content: center;-->
<!--                width: 100%;-->
<!--                border-bottom: 1.5px solid black;-->
<!--            }-->
<!--        }-->

<!--    @media (min-width: 800px) {-->
<!--        fieldset {-->
<!--            display: grid;-->
<!--                    grid-template-columns: auto auto;-->
<!--                    /*background-color: red;*/-->
<!--            max-width: 700px;-->
<!--            gap: 1rem;-->
<!--        }-->
<!--    }-->

<!--    /*.form-label {*/-->
<!--    /*    container-name: main;*/-->
<!--    /*    container-type: inline-size;*/-->
<!--    /*}*/-->
<!--    /*@container main (max-width: 700px) {*/-->
<!--    /*    .form-label {*/-->
<!--    /*        margin-top: 1.8rem;*/-->
<!--    /*        display: flex;*/-->
<!--    /*        flex-direction: column;*/-->
<!--    /*        justify-content: center;*/-->
<!--    /*        width: 100%;*/-->
<!--    /*        border-bottom: 1.5px solid black;*/-->
<!--    /*    }*/-->
<!--    /*}*/-->

<!--    /*@container main (min-width: 700px) {*/-->
<!--    /*    .form-label {*/-->
<!--    /*       display: grid;*/-->
<!--    /*        grid-template-columns: auto auto;*/-->
<!--    /*        background-color: red;*/-->

<!--    /*    }*/-->
<!--    /*}*/-->
<!--</style>-->