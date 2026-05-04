<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chapter 12: Plant Reproduction Mastery</title>
    <style>
        :root {
            --primary: #2e7d32;
            --secondary: #4caf50;
            --bg-color: #f1f8e9;
            --card-bg: #ffffff;
            --text-dark: #2c3e50;
            --accent: #ff9800;
            --danger: #e74c3c;
            --info: #3498db;
        }

        * { box-sizing: border-box; }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #a8e063 0%, #56ab2f 100%);
            color: var(--text-dark);
            margin: 0; padding: 20px;
            display: flex; justify-content: center; align-items: center;
            min-height: 100vh;
        }

        #app-container {
            background-color: var(--card-bg);
            border-radius: 20px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.3);
            max-width: 900px; width: 100%; padding: 35px;
            overflow: hidden; position: relative;
        }

        h1, h2, h3, h4 { color: var(--primary); margin-top: 0; }

        .header-image {
            width: 100%; height: 250px; object-fit: cover;
            border-radius: 12px; margin-bottom: 20px; box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .screen { display: none; animation: fadeIn 0.5s ease; }
        .screen.active { display: block; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

        .info-card {
            background: #f9fbe7; border-radius: 12px; padding: 20px; margin-bottom: 20px;
            border-left: 6px solid var(--secondary); text-align: left; line-height: 1.6;
        }

        .concept-highlight {
            background-color: #e8f5e9; padding: 10px; border-radius: 8px; font-weight: bold; color: var(--primary); margin: 10px 0;
        }

        .video-container {
            position: relative; padding-bottom: 56.25%; height: 0;
            margin: 15px 0 5px 0; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            background-color: #000;
        }
        .video-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0; }
        .video-fallback { text-align: center; font-size: 0.9em; margin-bottom: 20px; }
        .video-fallback a { color: var(--info); font-weight: bold; text-decoration: none; }
        .video-fallback a:hover { text-decoration: underline; }

        button {
            background-color: var(--primary); color: white; border: none; padding: 15px 20px;
            font-size: 1.1em; border-radius: 10px; cursor: pointer; transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            font-weight: bold; width: 100%; margin-top: 10px; z-index: 10; position: relative;
        }

        button:hover:not(:disabled) { background-color: #1b5e20; transform: translateY(-3px); box-shadow: 0 8px 20px rgba(0,0,0,0.2); }
        button:disabled { background-color: #bdc3c7; color: #ecf0f1; cursor: not-allowed; transform: none; box-shadow: none; }
        
        .btn-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px; }
        
        .stats-bar {
            display: flex; justify-content: space-between; background-color: var(--primary); color: white;
            padding: 12px 20px; border-radius: 10px 10px 0 0; font-weight: bold; font-size: 1.2em;
        }
        .progress-bar-bg { background-color: #e0e0e0; height: 10px; border-radius: 0 0 10px 10px; overflow: hidden; margin-bottom: 25px; }
        .progress-fill { background-color: var(--accent); height: 100%; width: 0%; transition: width 0.5s ease; }

        .score-pill { background: #fff; color: var(--primary); padding: 2px 8px; border-radius: 10px; font-size: 0.85em; margin-left: 10px; }
        .score-fail { color: var(--danger); }
        .score-pass { color: var(--secondary); }

        textarea {
            width: 100%; height: 130px; padding: 15px; border: 2px solid #ccc;
            border-radius: 10px; font-size: 1.05em; font-family: inherit; resize: vertical; margin-bottom: 15px;
            transition: border-color 0.3s;
        }
        textarea:focus { border-color: var(--primary); outline: none; }

        .match-row {
            display: flex; justify-content: space-between; align-items: center; background-color: #e8f5e9;
            padding: 12px 15px; margin-bottom: 10px; border-radius: 10px; font-weight: bold;
        }
        .match-row select { padding: 10px; border-radius: 8px; font-size: 1em; border: 2px solid var(--secondary); outline: none; cursor: pointer; }

        .feedback-box { padding: 20px; border-radius: 12px; margin-top: 20px; display: none; font-size: 1.05em; line-height: 1.6; animation: fadeIn 0.4s; }
        .feedback-correct { background-color: #e8f5e9; border: 2px solid #4caf50; color: #2e7d32; }
        .feedback-wrong { background-color: #ffebee; border: 2px solid #e74c3c; color: #c0392b; }
        
        .deep-dive { background-color: #e1f5fe; border-left: 5px solid var(--info); padding: 15px; margin-top: 15px; border-radius: 0 8px 8px 0; color: #0277bd;}
        .deep-dive h4 { margin: 0 0 8px 0; color: #01579b; font-size: 1.1em; }

        .badge { display: inline-block; padding: 6px 12px; border-radius: 20px; color: white; font-weight: bold; font-size: 0.85em; margin-bottom: 15px; }

        .locked-path { background-color: #34495e !important; }
        .locked-text { font-size: 0.85em; color: #bdc3c7; display: block; margin-top: 5px; font-weight: normal; }

        table { width: 100%; border-collapse: collapse; margin-top: 15px; background-color: white; font-size: 0.95em; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
        th, td { border: 1px solid #ddd; padding: 12px; text-align: left; vertical-align: top; }
        th { background-color: var(--danger); color: white; }
        tr:nth-child(even) { background-color: #f9f9f9; }
    </style>
</head>
<body>

<div id="app-container">

    <div id="screen-summary" class="screen active">
        <img src="https://images.unsplash.com/photo-1460533893735-45cea2212645?auto=format&fit=crop&w=1000" class="header-image" alt="Flowers">
        <h1>Chapter 12: DSE Core Summary</h1>
        <p>Master these fundamental rules before testing your knowledge. Your goal is to score at least 50 on both paths to unlock the final challenge!</p>

        <div class="video-container">
            <iframe src="https://www.youtube.com/embed/ExaQ8shhkw8" allowfullscreen></iframe>
        </div>
        <div class="video-fallback">
            <a href="https://youtu.be/ExaQ8shhkw8" target="_blank">📹 Video not loading? Click here to watch!</a>
        </div>
        
        <div class="info-card">
            <h4>🌸 Sexual Reproduction</h4>
            <div class="concept-highlight">Rule: Meiosis (forms gametes) + Mitosis (growth) = High Genetic Variation</div>
            <ul>
                <li><strong>The Sequence:</strong> 1. Gametes Form ➔ 2. Pollination ➔ 3. Pollen Tube Growth ➔ 4. Fertilization ➔ 5. Seed/Fruit Formation ➔ 6. Dispersal.</li>
                <li><strong>Fertilization Rule:</strong> Ovule ➔ Seed. Ovary Wall ➔ Fruit Wall.</li>
                <li><strong>Why Disperse?</strong> To prevent overcrowding, reduce competition for light/water with the parent, and colonize new environments.</li>
            </ul>
        </div>

        <div class="info-card">
            <h4>🥔 Asexual Reproduction (Vegetative)</h4>
            <div class="concept-highlight">Rule: Mitosis Only = Genetically Identical Clones</div>
            <ul>
                <li><strong>Pros & Cons:</strong> Fast and reliable (no wind or insects needed). But, a lack of genetic variation means the whole population is highly susceptible to the same diseases.</li>
                <li><strong>Storage Organs:</strong> 
                    <br>- <b>Bulb</b> (Onion: Fleshy leaves store food, dry leaves protect).
                    <br>- <b>Corm</b> (Gladiolus)
                    <br>- <b>Rhizome</b> (Ginger: horizontal underground stem)
                    <br>- <b>Stem Tuber</b> (Potato: swollen underground stem)
                </li>
            </ul>
        </div>

        <button id="btn-start">I've mastered the summary. Let's Begin! 🚀</button>
    </div>

    <div id="screen-path" class="screen">
        <div class="stats-bar">
            <span>Botanist Rank: <span id="ui-level">Seedling 🌱</span></span>
            <span>Total Points: <span id="ui-total-score">0</span></span>
        </div>
        <div class="progress-bar-bg"><div class="progress-fill" style="width: 100%;"></div></div>

        <img src="https://images.unsplash.com/photo-1471086569966-db3eebc25a59?auto=format&fit=crop&w=800" class="header-image" alt="Forest Path">
        <h2>Choose Your Botanical Path</h2>
        <p>You must score <strong>50 or higher</strong> on both Path A and Path B to unlock Path C.</p>
        
        <div class="btn-grid">
            <button id="btn-asexual" style="background-color: #8e44ad;">
                🥔 Path A: Asexual 
                <span id="score-pill-a" class="score-pill">Best: 0</span>
            </button>
            <button id="btn-sexual" style="background-color: #d35400;">
                🌸 Path B: Sexual
                <span id="score-pill-b" class="score-pill">Best: 0</span>
            </button>
        </div>
        
        <div style="border-top: 2px dashed #ccc; padding-top: 20px; margin-top: 10px;">
            <button id="btn-mixed" disabled class="locked-path">
                👑 Path C: Ultimate Mixed Mastery
                <span id="lock-text" class="locked-text">🔒 Requires 50+ on Path A & Path B</span>
            </button>
        </div>
    </div>

    <div id="screen-question" class="screen">
        <div class="stats-bar">
            <span id="path-title">Path</span>
            <span>Current Score: <span id="ui-current-score">0</span></span>
        </div>
        <div class="progress-bar-bg"><div id="q-progress" class="progress-fill"></div></div>
        
        <div id="q-badge" class="badge"></div>
        <h2 id="q-text" style="line-height: 1.4;">Question Text</h2>

        <div id="mc-options" class="btn-grid" style="display: none;"></div>

        <div id="long-answer-container" style="display: none;">
            <textarea id="long-answer-input" placeholder="Type your detailed DSE answer here..."></textarea>
            <button id="btn-submit-long">Submit Answer</button>
        </div>

        <div id="match-container" style="display: none;">
            <div id="match-rows"></div>
            <button id="btn-submit-match">Submit Pairings</button>
        </div>

        <div id="feedback-area" class="feedback-box"></div>
        <button id="btn-next" style="display: none; background-color: var(--accent); color: #fff;">Next Phase ➡️</button>
    </div>

    <div id="screen-result" class="screen" style="text-align: center;">
        <img src="https://images.unsplash.com/photo-1518531933037-91b2f5f229cc?auto=format&fit=crop&w=800" class="header-image" alt="Success Tree">
        <h1 style="font-size: 2.5em;">Path Complete! 🌟</h1>
        <h2>Score for this path: <span id="final-path-score"></span> / 100</h2>
        
        <div class="info-card" id="encouragement-text" style="text-align: center; font-size: 1.2em; border-left-color: var(--accent);">
        </div>

        <div id="wrong-answers-container" style="display: none; text-align: left; margin-top: 30px;">
            <h3 style="color: var(--danger); border-bottom: 2px solid var(--danger); padding-bottom: 10px;">⚠️ Review Your Mistakes</h3>
            <p style="color: var(--text-dark);">Reviewing these specific traps will guarantee you don't make them on the real DSE exam.</p>
            <div style="overflow-x: auto;">
                <table id="wrong-answers-table">
                    <thead>
                        <tr>
                            <th>Question</th>
                            <th>The Trap / Misconception</th>
                            <th>How to Avoid & Correct Concept</th>
                        </tr>
                    </thead>
                    <tbody id="wrong-answers-body">
                    </tbody>
                </table>
            </div>
            
            <div class="info-card" style="margin-top: 30px; border-left-color: var(--info); background-color: #e3f2fd;">
                <h3 style="color: var(--info); margin-top: 0;">📚 Master Advice for Studying Chapter 12</h3>
                <ul style="font-size: 1.05em; line-height: 1.6;">
                    <li><strong>Sequence is Key:</strong> Examiners love asking you to arrange events. Always remember: <em>Gametes form ➔ Pollination ➔ Pollen Tube ➔ Fertilization ➔ Seed/Fruit ➔ Dispersal.</em></li>
                    <li><strong>Beware the "Pollination vs. Dispersal" Trap:</strong> Pollination is for mixing genes (requires wind/insects BEFORE fertilization). Dispersal is for spreading out to avoid competition (requires wind/water/animals AFTER the fruit is formed).</li>
                    <li><strong>Memorize the Storage Organs:</strong> You must be able to instantly pair them. (Bulb = Onion, Corm = Gladiolus, Rhizome = Ginger, Tuber = Potato). Make flashcards for these!</li>
                    <li><strong>Cell Division Links:</strong> Whenever you see <em>Asexual/Vegetative</em>, immediately write down <strong>Mitosis (Clones)</strong>. Whenever you see <em>Sexual</em>, write down <strong>Meiosis (Variation)</strong>.</li>
                </ul>
            </div>
        </div>

        <button id="btn-return-paths" style="margin-top: 20px; background-color: var(--primary);">Return to Path Selection 🔙</button>
    </div>

</div>

<script>
    // FIX: Updated Question Constructor to correctly map 'options' and 'pairs' based on question type
    const q = (type, diff, color, text, data, extra, correctMsg, wrongMsg, trap, avoid) => {
        return {
            type: type, 
            difficulty: diff, 
            color: color, 
            text: text, 
            options: type === 'match' ? extra : data, 
            pairs: type === 'match' ? data : null, 
            keywords: type === 'long' ? extra : [], 
            correctMsg: correctMsg, 
            wrongMsg: wrongMsg, 
            trap: trap, 
            avoid: avoid
        };
    };

    const asexualQuestions = [
        q("mc", "Easy", "#4caf50", "According to your notes, which cell division process is solely responsible for vegetative propagation?", 
            [{text: "Meiosis", correct: false}, {text: "Mitosis", correct: true}, {text: "Binary Fission", correct: false}], [],
            "Spot on! Asexual reproduction in plants relies entirely on Mitosis.", "Incorrect. Meiosis is for gametes.", 
            "Confusing meiosis with mitosis.", "Mnemonic: 'Mi-TOE-sis' makes exact copies (like growing a toe cell). 'ME-iosis' makes ME (reproduction)."),
        
        q("mc", "Easy", "#4caf50", "Which of the following organisms reproduces exclusively via binary fission?", 
            [{text: "Amoeba", correct: true}, {text: "Gladiolus", correct: false}, {text: "Strawberry", correct: false}], [],
            "Correct! Amoeba is a single-celled organism using binary fission.", "Plants use vegetative organs. Amoeba uses fission.", 
            "Assuming plants use binary fission.", "Binary fission = bacteria/amoeba splitting in two. Plants use vegetative propagation."),
        
        q("match", "Medium", "#ff9800", "Pair the correct specialized storage organ with its textbook example:", 
            [{item: "Bulb", match: "Onion"}, {item: "Corm", match: "Gladiolus"}, {item: "Rhizome", match: "Ginger"}, {item: "Stem Tuber", match: "Potato"}], ["Potato", "Onion", "Ginger", "Gladiolus"],
            "Perfect! You nailed the DSE examples.", "Review the specific plant examples from Chapter 12.", 
            "Mixing up Rhizome (Ginger) and Corm (Gladiolus).", "Memorize the list exactly: Bulb=Onion, Corm=Gladiolus, Rhizome=Ginger, Tuber=Potato."),
        
        q("mc", "Medium", "#ff9800", "Why are offspring produced by vegetative propagation described as 'clones'?", 
            [{text: "They grow in the exact same location.", correct: false}, {text: "They are genetically identical to the parent and each other.", correct: true}], [],
            "Correct. No gamete fusion means no genetic mixing.", "Clones refers to their DNA, not their location.", 
            "Thinking 'clone' just means looking similar.", "In biology, 'clone' strictly means 100% identical genetic makeup due to mitosis."),
        
        q("long", "Hard (DSE)", "#e74c3c", "State ONE major advantage and ONE major risk of a farmer exclusively using artificial vegetative propagation.", 
            null, ["fast", "identical", "retain", "disease", "wipe out", "variation", "clone"], 
            "Advantage: Fast/Retains traits. Risk: No genetic variation against diseases.", "You missed the core concepts of retention and variation.", 
            "Listing 'overcrowding' as the main risk for farmers.", "Farmers control spacing! The real biological risk is lack of genetic variation against new diseases."),
        
        q("mc", "Medium", "#ff9800", "In artificial tissue culture, what two specific things must the agar medium contain to stimulate plantlet growth?", 
            [{text: "Chlorophyll & Water", correct: false}, {text: "Nutrients & Auxins", correct: true}, {text: "Pollen & Nectar", correct: false}], [],
            "Correct! Nutrients feed it, Auxins (hormones) stimulate cell division.", "It requires specific chemicals.", 
            "Forgetting 'Auxins'.", "Auxins are the essential plant growth hormones needed to force unspecialized tissue to divide."),
        
        q("match", "Medium", "#ff9800", "Pair the parts of an Onion Bulb to their biological functions:", 
            [{item: "Fleshy scale leaf", match: "Stores food"}, {item: "Dry scale leaf", match: "Protection"}, {item: "Bud", match: "Develops into shoot"}], ["Protection", "Develops into shoot", "Stores food"],
            "Great anatomy knowledge!", "Fleshy=Food, Dry=Protect, Bud=Shoot.", 
            "Thinking the dry brown skin stores food.", "The dry skin is dead tissue for protection. The juicy, fleshy inner layers store the food!"),
        
        q("mc", "Easy", "#4caf50", "During harsh winter conditions, which part of a potato plant survives to sprout the following spring?", 
            [{text: "The underground stem tuber", correct: true}, {text: "The aerial green leaves", correct: false}], [],
            "Correct! The aerial parts die, but the underground tuber remains dormant.", "The green leaves die off in the cold.", 
            "Assuming the entire plant dies.", "Storage organs specifically evolved as an underground survival mechanism for harsh winters."),
        
        q("mc", "Easy", "#4caf50", "Taking a portion of a stem and placing it directly into soil is an artificial method called:", 
            [{text: "Grafting", correct: false}, {text: "Cutting", correct: true}], [],
            "Correct! Cutting is the simplest artificial method.", "Grafting involves attaching two different plants together.", 
            "Confusing Cutting with Grafting.", "Cutting = Cut and plant in soil. Grafting = Cut and tape to another plant's stem."),
        
        q("long", "Hard (DSE)", "#e74c3c", "Explain biologically why asexual reproduction is generally faster and more reliable than sexual reproduction.", 
            null, ["external agent", "pollination", "dispersal", "wind", "insect"], 
            "It does not rely on external agents (like wind/insects) for pollination or dispersal.", "It avoids the waiting period for external agents.", 
            "Saying 'mitosis is faster'.", "The DSE marking scheme strictly looks for 'does not require external agents for pollination/dispersal'.")
    ];

    const sexualQuestions = [
        q("mc", "Easy", "#4caf50", "Which two parts collectively make up the male Stamen of a flower?", 
            [{text: "Stigma & Style", correct: false}, {text: "Anther & Filament", correct: true}], [],
            "Correct! Stamen = Anther + Filament.", "Stigma and Style are part of the female Carpel.", 
            "Confusing male and female parts.", "Mnemonic: staMEN (Male) = Anther + Filament."),
        
        q("mc", "Easy", "#4caf50", "Following successful fertilization, what specific floral structure transforms into the Seed?", 
            [{text: "The Ovule", correct: true}, {text: "The Ovary wall", correct: false}], [],
            "Correct! Ovule -> Seed.", "The ovary wall becomes the fruit.", 
            "Mixing up Ovule and Ovary.", "OvulE becomes the SEEd. OvARY becomes the Fruit."),
        
        q("match", "Medium", "#ff9800", "Pair the outer floral parts to their correct functions:", 
            [{item: "Sepal (Calyx)", match: "Protects flower bud"}, {item: "Petal", match: "Attracts insects"}, {item: "Nectary", match: "Produces sugary liquid"}], ["Produces sugary liquid", "Protects flower bud", "Attracts insects"],
            "Excellent matching!", "Sepal protects, Petal attracts, Nectary rewards.", 
            "Confusing the Sepal with the Petal.", "Sepals are the small green leaf-like structures at the base that protect the bud before it opens."),
        
        q("long", "Hard (DSE)", "#e74c3c", "Describe the physical adaptations of the stigma in wind-pollinated flowers compared to insect-pollinated flowers.", 
            null, ["feathery", "outside", "large", "sticky", "inside"], 
            "Wind: Large, feathery, hanging outside. Insect: Sticky, located inside.", "Wind needs nets (feathery), insects need glue (sticky).", 
            "Stating wind flowers need nectar.", "Wind does not have a brain; it is not attracted by nectar!"),
        
        q("mc", "Medium", "#ff9800", "What is the primary evolutionary advantage of cross-pollination?", 
            [{text: "It results in greater genetic variation.", correct: true}, {text: "It prevents overcrowding.", correct: false}], [],
            "Correct! Variation helps species survive changing environments.", "Overcrowding is solved by seed dispersal, not pollination.", 
            "Confusing the benefits of pollination with dispersal.", "Pollination = Gene mixing (Variation). Dispersal = Space mixing (Avoiding overcrowding)."),
        
        q("mc", "Medium", "#ff9800", "Biologically, what makes an apple a 'false fruit'?", 
            [{text: "It does not contain real seeds.", correct: false}, {text: "It develops from the receptacle, not the ovary wall.", correct: true}], [],
            "Correct! True fruits develop exclusively from the ovary.", "False fruits still have real seeds.", 
            "Assuming false fruits are seedless.", "'False' just refers to the tissue of origin (the receptacle base swells up, not the ovary)."),
        
        q("match", "Medium", "#ff9800", "Pair the seed dispersal method to its physical plant adaptation:", 
            [{item: "Wind", match: "Wing-like structures"}, {item: "Water", match: "Buoyant spaces"}, {item: "Animal", match: "Hooks / Fleshy"}], ["Hooks / Fleshy", "Wing-like structures", "Buoyant spaces"],
            "Perfect adaptations knowledge!", "Wind=Wings, Water=Buoyant, Animal=Fleshy/Hooks.", 
            "Assuming fleshy fruits are just for humans.", "Plants evolved fleshy fruits specifically so animals eat them and poop the seeds far away!"),
        
        q("long", "Hard (DSE)", "#e74c3c", "Explain two vital ecological reasons why seed dispersal is necessary for plant survival.", 
            null, ["overcrowding", "competition", "light", "water", "colonize"], 
            "It prevents overcrowding/competition with the parent, and allows colonization of new habitats.", "Dispersal spreads the offspring out.", 
            "Confusing dispersal with pollination.", "Pollination happens BEFORE fertilization. Dispersal happens AFTER the fruit is completely formed."),
        
        q("mc", "Easy", "#4caf50", "After a pollen grain lands on a compatible stigma, what structure actively grows down the style?", 
            [{text: "The Pollen Tube", correct: true}, {text: "The Male Gamete itself", correct: false}], [],
            "Correct! The pollen tube acts as a tunnel for the gamete.", "The gamete doesn't swim down on its own.", 
            "Thinking the pollen grain falls into the ovary.", "The grain stays stuck on top of the stigma; it grows a long 'tube' down the style."),
        
        q("mc", "Medium", "#ff9800", "DSE Trap: Are pollen grains the actual male gametes of the plant?", 
            [{text: "Yes", correct: false}, {text: "No", correct: true}], [],
            "Correct! Pollen grains CARRY the male gametes.", "Pollen grains are the carrier structures, not the gametes.", 
            "Directly calling a pollen grain a gamete.", "This is the most common DSE trap! The pollen grain is the 'spaceship', the gamete is the 'astronaut' inside.")
    ];

    const mixedQuestions = [
        q("mc", "Hard", "#8e44ad", "MIXED: Which statement correctly compares the cell divisions involved in both reproduction types?", 
            [{text: "Asexual uses meiosis; Sexual uses mitosis.", correct: false}, {text: "Asexual uses mitosis only; Sexual involves meiosis (for gametes) and mitosis.", correct: true}], [],
            "Correct! Sexual reproduction requires meiosis to halve the chromosomes.", "Asexual uses Mitosis. Sexual requires Meiosis.", 
            "Flipping the definitions.", "Asexual (A = 1 parent) = Mitosis. Sexual (S = Sex cells) = Meiosis."),
        
        q("long", "Hard (DSE)", "#e74c3c", "MIXED: Arrange these processes in chronological order: Seed Dispersal, Pollination, Fertilization, Formation of Gametes.", 
            null, ["gamete", "pollination", "fertilization", "dispersal"], 
            "1. Gametes -> 2. Pollination -> 3. Fertilization -> 4. Dispersal.", "You missed the correct sequence. Review the steps.", 
            "Putting fertilization before pollination.", "You must deliver the mail (pollination) before you can open it (fertilization)!"),
        
        q("match", "Hard", "#8e44ad", "MIXED: Match the biological process to the reproduction type:", 
            [{item: "Requires External Agents", match: "Sexual"}, {item: "Produces Genetic Clones", match: "Asexual"}, {item: "High Risk of Overcrowding", match: "Asexual"}], ["Asexual", "Sexual", "Asexual"],
            "Excellent understanding of the differences!", "Sexual needs agents; Asexual makes clones & overcrowds.", 
            "Thinking sexual reproduction causes more overcrowding.", "Sexual seeds disperse. Asexual tubers grow right next to the parent!"),
        
        q("mc", "Hard", "#8e44ad", "MIXED: What are the two main sources of genetic variation in sexual reproduction?", 
            [{text: "Mitosis and cloning", correct: false}, {text: "Meiosis and random fertilization", correct: true}], [],
            "Correct! Meiosis shuffles the genes, and fertilization is random.", "Variation comes from Meiosis and random fertilization.", 
            "Forgetting 'random fertilization'.", "Both the creation of unique gametes AND the random chance of which pollen meets which ovule create variation."),
        
        q("long", "Hard (DSE)", "#e74c3c", "MIXED: Explain why a forest grown from dispersed seeds is more likely to survive a new fungal infection than a farm field grown from potato tubers.", 
            null, ["variation", "seeds", "sexual", "resistant", "survive", "identical", "clones"], 
            "Seeds have genetic variation, so some may be naturally resistant. Tubers are identical clones; if one is susceptible, all will die.", "Seeds (sexual) = Variation. Tubers (asexual) = Clones.", 
            "Answering that potatoes have weak immune systems.", "It has nothing to do with plant strength; it is entirely about GENETIC diversity!"),
        
        q("mc", "Hard", "#8e44ad", "MIXED: Which of the following processes relies completely on independent assortment?", 
            [{text: "Vegetative Propagation", correct: false}, {text: "Pollen and Ovule formation", correct: true}], [],
            "Correct! Independent assortment is a Meiosis concept.", "Meiosis creates pollen/ovules.", 
            "Not recognizing meiosis vocabulary.", "Independent assortment and crossing over ONLY happen in Meiosis (Sexual reproduction)."),
        
        q("match", "Hard", "#8e44ad", "MIXED: Pair the microscopic structure to its ultimate fate after fertilization:", 
            [{item: "Ovule", match: "Becomes Seed"}, {item: "Ovary Wall", match: "Becomes Fruit Wall"}, {item: "Pollen Tube", match: "Degenerates"}], ["Becomes Fruit Wall", "Degenerates", "Becomes Seed"],
            "Flawless DSE biology!", "Ovule->Seed, Ovary->Fruit, Tube->Degenerates.", 
            "Thinking the pollen tube becomes part of the seed.", "Once the tube delivers the male gamete, its job is done and it dies (degenerates)."),
        
        q("mc", "Hard", "#8e44ad", "MIXED: Is 'Self-pollination' considered Sexual or Asexual reproduction?", 
            [{text: "Sexual, because it involves the fusion of gametes.", correct: true}, {text: "Asexual, because there is only one parent plant.", correct: false}], [],
            "Correct! It involves male and female gametes, so it is Sexual!", "If it uses gametes, it is Sexual.", 
            "Assuming 1 parent = Asexual.", "Even though it's one plant, it produces MALE pollen and FEMALE ovules that fuse. Gamete fusion = Sexual."),
        
        q("mc", "Hard", "#8e44ad", "MIXED: Which method will help a plant species colonize a newly formed volcanic island?", 
            [{text: "Producing stem tubers", correct: false}, {text: "Producing buoyant seeds", correct: true}], [],
            "Correct! Seeds can travel across oceans; tubers cannot.", "Water dispersal of seeds allows colonization.", 
            "Tubers can't cross oceans.", "Vegetative propagation keeps offspring physically attached. Seeds are built for travel!"),
        
        q("long", "Hard (DSE)", "#e74c3c", "MIXED: State the fundamental difference in the offspring produced by binary fission versus cross-pollination.", 
            null, ["identical", "clones", "variation", "different"], 
            "Binary fission produces identical clones. Cross-pollination produces offspring with high genetic variation.", "Fission = clones. Cross-pollination = variation.", 
            "Writing a long paragraph without hitting the core keywords.", "In DSE Biology, keep it direct: Fission = Identical. Cross-pollination = Variation.")
    ];

    // Global State Variables
    let currentQList = [];
    let qIndex = 0;
    let currentPathScore = 0;
    let wrongAnswersList = []; 
    
    let highScoreA = 0;
    let highScoreB = 0;
    let totalScore = 0;

    // DOM Elements
    const screens = {
        summary: document.getElementById('screen-summary'),
        path: document.getElementById('screen-path'),
        question: document.getElementById('screen-question'),
        result: document.getElementById('screen-result')
    };

    document.addEventListener("DOMContentLoaded", () => {
        document.getElementById('btn-start').addEventListener('click', () => switchScreen('path'));
        
        document.getElementById('btn-asexual').addEventListener('click', () => startPath(asexualQuestions, "Path A: Asexual"));
        document.getElementById('btn-sexual').addEventListener('click', () => startPath(sexualQuestions, "Path B: Sexual"));
        document.getElementById('btn-mixed').addEventListener('click', () => startPath(mixedQuestions, "Path C: Mixed Mastery"));
        
        document.getElementById('btn-return-paths').addEventListener('click', () => {
            checkUnlock();
            switchScreen('path');
        });

        document.getElementById('btn-next').addEventListener('click', () => {
            qIndex++;
            if(qIndex < currentQList.length) {
                renderQuestion();
            } else {
                endPath();
            }
        });
    });

    function switchScreen(screenName) {
        Object.values(screens).forEach(s => s.classList.remove('active'));
        screens[screenName].classList.add('active');
        window.scrollTo(0,0);
    }

    function checkUnlock() {
        const mixedBtn = document.getElementById('btn-mixed');
        const lockText = document.getElementById('lock-text');
        
        if(highScoreA >= 50 && highScoreB >= 50) {
            mixedBtn.disabled = false;
            mixedBtn.classList.remove('locked-path');
            mixedBtn.style.backgroundColor = "#e67e22";
            lockText.innerText = "👑 UNLOCKED: Prepare for the ultimate DSE test!";
            lockText.style.color = "#fff";
        }
    }

    function startPath(qArray, title) {
        currentQList = qArray;
        qIndex = 0;
        currentPathScore = 0;
        wrongAnswersList = []; 
        
        document.getElementById('path-title').innerText = title;
        document.getElementById('ui-current-score').innerText = currentPathScore;
        switchScreen('question');
        renderQuestion();
    }

    function updateScore(pts) {
        currentPathScore += pts;
        document.getElementById('ui-current-score').innerText = currentPathScore;
    }

    function updateProgressBar() {
        const percent = ((qIndex) / currentQList.length) * 100;
        document.getElementById('q-progress').style.width = percent + '%';
    }

    function renderQuestion() {
        updateProgressBar();
        const q = currentQList[qIndex];
        const fbArea = document.getElementById('feedback-area');
        fbArea.style.display = 'none';
        document.getElementById('btn-next').style.display = 'none';
        
        document.getElementById('mc-options').style.display = 'none';
        document.getElementById('long-answer-container').style.display = 'none';
        document.getElementById('match-container').style.display = 'none';
        
        document.getElementById('q-badge').innerText = `Question ${qIndex+1}/10 - ${q.difficulty}`;
        document.getElementById('q-badge').style.backgroundColor = q.color;
        document.getElementById('q-text').innerText = q.text;

        if(q.type === 'mc') {
            const mcBox = document.getElementById('mc-options');
            mcBox.style.display = 'grid'; mcBox.innerHTML = '';
            q.options.forEach(opt => {
                let btn = document.createElement('button');
                btn.innerText = opt.text;
                btn.onclick = () => handleAnswer(opt.correct, btn, q);
                mcBox.appendChild(btn);
            });
        } else if(q.type === 'long') {
            document.getElementById('long-answer-container').style.display = 'block';
            document.getElementById('long-answer-input').value = '';
            
            let btnSubmit = document.getElementById('btn-submit-long');
            let newBtn = btnSubmit.cloneNode(true);
            btnSubmit.parentNode.replaceChild(newBtn, btnSubmit);
            newBtn.disabled = false;
            
            newBtn.onclick = () => {
                const ans = document.getElementById('long-answer-input').value.toLowerCase().trim();
                let matches = q.keywords.filter(kw => ans.includes(kw)).length;
                handleAnswer(matches >= 2, newBtn, q);
            };
        } else if(q.type === 'match') {
            document.getElementById('match-container').style.display = 'block';
            const mRows = document.getElementById('match-rows'); mRows.innerHTML = '';
            
            let btnSubmit = document.getElementById('btn-submit-match');
            let newBtn = btnSubmit.cloneNode(true);
            btnSubmit.parentNode.replaceChild(newBtn, btnSubmit);
            newBtn.disabled = false;
            
            let selHTML = `<option value="">-- Select Match --</option>`;
            q.options.forEach(o => selHTML += `<option value="${o}">${o}</option>`);

            q.pairs.forEach((pair, i) => {
                let div = document.createElement('div'); div.className = 'match-row';
                div.innerHTML = `<span>${pair.item}</span> <select id="msel-${i}">${selHTML}</select>`;
                mRows.appendChild(div);
            });
            
            newBtn.onclick = () => {
                let allCorrect = true;
                q.pairs.forEach((p, i) => { if(document.getElementById(`msel-${i}`).value !== p.match) allCorrect = false; });
                handleAnswer(allCorrect, newBtn, q);
            };
        }
    }

    function handleAnswer(isCorrect, btn, q) {
        if(btn.tagName === 'BUTTON') btn.disabled = true;
        if(q.type === 'mc') document.querySelectorAll('#mc-options button').forEach(b => b.disabled = true);
        
        if(isCorrect) {
            updateScore(10);
        } else {
            wrongAnswersList.push(q);
        }
        
        const fbArea = document.getElementById('feedback-area');
        fbArea.style.display = 'block';
        fbArea.className = isCorrect ? 'feedback-box feedback-correct' : 'feedback-box feedback-wrong';
        
        let fbHTML = isCorrect ? `<strong>🎉 Brilliant! (+10 pts)</strong><br>${q.correctMsg}` : `<strong>❌ Let's review this.</strong><br>${q.wrongMsg}`;
        
        if(!isCorrect) {
            fbHTML += `
            <div class="deep-dive">
                <h4>⚠️ Common Careless Trap</h4>
                <p>${q.trap}</p>
                <h4>🛡️ How to Avoid in DSE</h4>
                <p>${q.avoid}</p>
            </div>`;
        }
        
        fbArea.innerHTML = fbHTML;
        document.getElementById('btn-next').style.display = 'block';
        
        setTimeout(() => { fbArea.scrollIntoView({ behavior: 'smooth', block: 'nearest' }); }, 100);
    }

    function endPath() {
        if(currentQList === asexualQuestions && currentPathScore > highScoreA) {
            highScoreA = currentPathScore;
            const pillA = document.getElementById('score-pill-a');
            pillA.innerText = `Best: ${highScoreA}`;
            pillA.className = highScoreA >= 50 ? 'score-pill score-pass' : 'score-pill score-fail';
        }
        if(currentQList === sexualQuestions && currentPathScore > highScoreB) {
            highScoreB = currentPathScore;
            const pillB = document.getElementById('score-pill-b');
            pillB.innerText = `Best: ${highScoreB}`;
            pillB.className = highScoreB >= 50 ? 'score-pill score-pass' : 'score-pill score-fail';
        }
        
        totalScore = highScoreA + highScoreB + (currentQList === mixedQuestions ? currentPathScore : 0);
        document.getElementById('ui-total-score').innerText = totalScore;
        
        let level = "Seedling 🌱";
        if(totalScore >= 50) level = "Sprouting Plant 🌿";
        if(totalScore >= 100) level = "Flowering Botanist 🌸";
        if(totalScore >= 250) level = "Master Tree 🌳👑";
        document.getElementById('ui-level').innerText = level;

        document.getElementById('final-path-score').innerText = currentPathScore;
        const msgEl = document.getElementById('encouragement-text');
        
        if(currentPathScore >= 50) {
            msgEl.innerHTML = "<strong>Excellent growth! 🌻</strong><br>You have shown a strong understanding of these biological concepts. Remember, every mistake is just fertilizer for your brain.";
        } else {
            msgEl.innerHTML = "<strong>Keep watering your mind! 💧</strong><br>You didn't reach the 50 point requirement yet, but that's exactly why we practice! Review your mistakes in the table below and try again. You've got this!";
        }

        const wrongContainer = document.getElementById('wrong-answers-container');
        const wrongBody = document.getElementById('wrong-answers-body');
        
        if (wrongAnswersList.length > 0) {
            wrongContainer.style.display = 'block';
            wrongBody.innerHTML = ''; 
            
            wrongAnswersList.forEach(q => {
                wrongBody.innerHTML += `
                    <tr>
                        <td><strong>${q.text}</strong></td>
                        <td style="color: #c0392b;">${q.trap}</td>
                        <td style="color: #27ae60;"><strong>Rule:</strong> ${q.avoid}<br><br><em style="color:#555;">Fact: ${q.correctMsg}</em></td>
                    </tr>
                `;
            });
        } else {
            wrongContainer.style.display = 'block';
            wrongBody.innerHTML = `<tr><td colspan="3" style="text-align:center; color: #2e7d32; font-size: 1.2em; padding: 20px;"><strong>Flawless Victory! 🏆 You didn't make a single mistake on this path!</strong></td></tr>`;
        }

        switchScreen('result');
    }
</script>

</body>
</html>
