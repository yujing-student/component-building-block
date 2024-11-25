<script>
    import TextButton from '$lib/Subscribe.svelte';
    import {onMount} from 'svelte';

    // onMount( () => {
    //
    //     let texteare = document.querySelector('textarea');
    //     let select = document.querySelector('select');
    //
    //
    // });


    // als het input field leeg is voeg een border-bottom toe met add class
    //event prevault
    //     todo met javascript verplicht maken van de fte en de texteare
</script>
<h1>INSCHRIJVEN</h1>

<form action="/bedankt">

    <!--     todo met css steertetje maken befoe en after -->
    <fieldset>
        <legend>persoonlijke gegevens</legend>
        <label class="form-label" for="functie">

                        <span class="star">       Functie</span>
            <input aria-required="true" id="functie" required type="text"/>
        </label>
        <label class="form-label" for="Voornaam">
                        <span class="star">Voornaam</span>
            <input aria-required="true" id="Voornaam" required type="text"
            />
        </label>
        <label class="form-label" for="Tussenvoegsel">
            Tussenvoegsel
            <input id="Tussenvoegsel" type="text"/>
        </label>
        <label class="form-label" for="Achternaam">

            <span class="star">Achternaam</span>
            <input aria-required="true" id="Achternaam" required type="text"/>
        </label>

        <label class="form-label" for="email">

                        <span class="star">E-mail</span>
            <input aria-required="true" id="email" required type="email"/>

        </label>
        <label class="form-label" for="Mobiel">

                        <span class="star">  Mobiel</span>
            <input aria-required="true" id="Mobiel"
                   required
                   type="number"/>
        </label>
        <label class="form-label" for="Bedrijfsnaam">

                        <span class="star">Bedrijfsnaam</span>
            <input aria-required="true" id="Bedrijfsnaam" required type="text"/>
        </label>
        <label class="form-label " for="Bedrijfswebsite">

                        <span class="star">Bedrijfswebsite</span>
            <input aria-required="true" id="Bedrijfswebsite" required type="text"/>
        </label>


        <label class="form-label input-textfield" for="ik-wil-graag-lid-worden-omdat">
                  <span class="star">Ik wil graag lid worden omdat </span>


            <textarea  cols="5" rows="1" placeholder="" aria-required="true"
                       required></textarea>
        </label>

        <label class="dropown" for="FTE">

                        <span class="star">      FTE</span>
            <select aria-required="true" id="FTE" required>
                <option disabled hidden selected value="-1"></option>
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

    form {
        color: var(--grey);
    }

    fieldset {
        border: none;
    }

    legend {
        position: absolute;
        top: 0;
        left: -9999px;
    }

    label {
        margin-top: 1.8rem;
        display: grid;
        width: 100%;
        border-bottom: 1.5px solid var(--black);
        gap: 0.8rem;
    }
    span{
        grid-row: 1;
        grid-column: 1;

    }
    input{
        grid-row: 2;
        grid-column-start: 1;
        grid-column-end: 3;
    }

    input, textarea, select {
        border: none;
    }


    textarea {
        height: auto;
    }

    .star:after{
        content: "*";
        font-size: 2rem;
        color: red;

    }


    /*ui states*/
    input:focus, textarea:focus, select:focus, option:focus {
        outline: 2px solid var(--blue);
    }

    textarea {
        width: 100%; /* Make it full width */
    }

    /*input[type="email"]:user-invalid, input:user-invalid {*/
    /*    !*border-bottom: 3px solid red;*!*/
    /*    outline: 3px solid red;*/
    /*}*/

    /*input:user-valid {*/
    /*    outline: 2px solid green;*/
    /*}*/

    /*select:user-invalid {*/
    /*    outline: 2px solid red;*/
    /*}*/
    /*select:user-valid {*/
    /*    outline: 2px solid green;*/
    /*}*/
    /*option:user-invalid {*/
    /*    outline: 2px solid red;*/
    /*}*/
    /*option:user-valid {*/
    /*    outline: 2px solid green;*/
    /*}*/



    /* form focus valid  */

    input[type='text']:user-valid,
    input[type='email']:valid,
    input[type='number']:valid,
    textarea:valid,
    select:user-valid,
    option:user-valid
    {
        outline: 2px solid green;

    }

    /* form focus invalid */

    input[type='text']:user-invalid,
    input[type='email']:user-invalid,
    input[type='number']:user-invalid,
    textarea:user-invalid,
    select:user-invalid

    {
        outline: 2px solid red;
    }

    /*textarea{*/
    /*    border: none;*/
    /*    padding: 0.5rem;*/
    /*    border-radius: var(--border-card);*/
    /*    outline: none;*/
    /*    !* box-shadow: 0px 2px 4px hsl(32 37% 39% / 1); *!*/
    /*    outline: 1px solid var(--input-border-color);*/
    /*    position: relative;*/
    /*    z-index: 100;*/
    /*}*/
    /*textarea:valid {*/
    /*    outline: 2px solid green;*/
    /*}*/

    /*textarea:user-invalid {*/
    /*    outline: 2px solid red;*/
    /*    !* background: #FFEFEF; *!*/
    /*}*/



    form {
        container-type: inline-size;
    }

    @container  (min-width: 600px) {
        fieldset {
            display: grid;
            grid-template-columns: auto auto;
            max-width: 700px;
            gap: 1rem;
        }

        .input-textfield {
            grid-row: 6;
            grid-column-start: 1;
            grid-column-end: 3;
        }

        .dropown {
            grid-row: 7;
        }
    }

</style>


