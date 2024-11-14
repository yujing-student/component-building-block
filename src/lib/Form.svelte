
<script>
    import TextButton from '$lib/Subscribe.svelte'
</script>

<form>
    <fieldset>
        <legend>persoonlijke gegevens</legend>
        <label for="Voornaam" class="form-label">
            Voornaam*
            <input id="Voornaam"  type="text" required

            />
        </label>
        <label for="Tussenvoegsel" class="form-label">
            Tussenvoegsel
            <input id="Tussenvoegsel" type="text"/>
        </label>
        <label for="Achternaam" class="form-label">
            Achternaam*
            <input id="Achternaam"  type="text"/>
        </label>
        <label for="functie" class="form-label">
            Functie*
            <input id="functie" type="text"/>
        </label>
        <label for="email" class="form-label">
            E-mail*
            <input id="email" type="email"/>
        </label>
        <label for="Mobiel" class="form-label">
            Mobiel*
            <input id="Mobiel"  type="tel"/>
        </label>
        <label for="Bedrijfsnaam" class="form-label">
            Bedrijfsnaam*
            <input id="Bedrijfsnaam"  type="text"/>
        </label>
        <label for="Bedrijfswebsite" class="form-label">
            Bedrijfswebsite*
            <input id="Bedrijfswebsite"    type="text"/>
        </label>
        <label for="ik wil graag lid worden omdat" class="form-label ">
            ik wil graag lid worden omdat*
            <textarea>

            </textarea>
        </label>
        <label for="FTE">
            FTE*
            <select id="FTE" >
                <option value="">

                </option>
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