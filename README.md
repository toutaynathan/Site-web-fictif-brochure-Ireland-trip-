# Site-web-fictif-brochure-Ireland-trip-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover Ireland - The Emerald Isle Adventure</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: #2d5016;
            background: linear-gradient(135deg, #4a7c59 0%, #6b8e23 100%);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400"><rect fill="%23228B22" width="1200" height="400"/><circle fill="%2332CD32" cx="200" cy="150" r="80" opacity="0.6"/><circle fill="%2390EE90" cx="800" cy="250" r="120" opacity="0.4"/><circle fill="%23006400" cx="1000" cy="100" r="60" opacity="0.8"/></svg>');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 100px 0;
            position: relative;
        }

        .slogan {
            font-size: 3.5em;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
            margin-bottom: 20px;
            animation: fadeInUp 2s ease-out;
        }

        .tagline {
            font-size: 1.5em;
            font-style: italic;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.7);
            animation: fadeInUp 2s ease-out 0.5s both;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Navigation */
        nav {
            background: #1a4d2e;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 40px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1em;
            padding: 10px 20px;
            border-radius: 25px;
            transition: all 0.3s ease;
        }

        nav a:hover {
            background: #4a7c59;
            transform: translateY(-2px);
        }

        /* Section Styles */
        section {
            padding: 80px 0;
            background: white;
            margin: 40px 0;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        section:nth-child(even) {
            background: linear-gradient(135deg, #f0f8f0 0%, #e8f5e8 100%);
        }

        h2 {
            font-size: 2.8em;
            text-align: center;
            margin-bottom: 50px;
            color: #1a4d2e;
            position: relative;
        }

        h2::after {
            content: '';
            width: 100px;
            height: 4px;
            background: #4a7c59;
            display: block;
            margin: 20px auto;
            border-radius: 2px;
        }

        h3 {
            color: #2d5016;
            font-size: 1.8em;
            margin: 30px 0 15px;
            border-left: 4px solid #4a7c59;
            padding-left: 20px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }

        .card {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 2px solid transparent;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            border-color: #4a7c59;
        }

        .image-placeholder {
            width: 100%;
            height: 200px;
            background: linear-gradient(45deg, #4a7c59, #6b8e23);
            border-radius: 10px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2em;
            font-weight: bold;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        /* Road Trip Section */
        .road-trip {
            background: linear-gradient(135deg, #2d5016 0%, #1a4d2e 100%);
            color: white;
            border-radius: 20px;
            padding: 60px;
            margin: 60px 0;
        }

        .itinerary {
            display: grid;
            gap: 40px;
            margin-top: 40px;
        }

        .day {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 15px;
            border-left: 5px solid #4a7c59;
            backdrop-filter: blur(10px);
        }

        .day h4 {
            font-size: 1.5em;
            margin-bottom: 15px;
            color: #90EE90;
        }

        /* Call to Action */
        .cta {
            background: linear-gradient(135deg, #ff6b35 0%, #f7931e 100%);
            color: white;
            padding: 60px;
            text-align: center;
            border-radius: 20px;
            margin: 60px 0;
        }

        .cta-button {
            display: inline-block;
            background: white;
            color: #ff6b35;
            padding: 15px 40px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.2em;
            margin-top: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
        }

        /* Footer */
        footer {
            background: #1a4d2e;
            color: white;
            text-align: center;
            padding: 40px 0;
            margin-top: 60px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .slogan {
                font-size: 2.5em;
            }
            
            nav ul {
                flex-direction: column;
                gap: 10px;
            }
            
            .grid {
                grid-template-columns: 1fr;
            }
            
            .road-trip {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1 class="slogan">🍀 Ireland Awaits You! 🍀</h1>
            <p class="tagline">"Where every corner tells a story and every landscape steals your heart"</p>
        </div>
    </header>

    <nav>
        <ul>
            <li><a href="#natural">🏔️ Natural Wonders</a></li>
            <li><a href="#cultural">🎭 Cultural Heritage</a></li>
            <li><a href="#traditions">🎪 Traditions</a></li>
            <li><a href="#screen">🎬 Screen Tourism</a></li>
            <li><a href="#roadtrip">🚗 Road Trip</a></li>
        </ul>
    </nav>

    <div class="container">
        <section id="natural">
            <h2>🌿 Natural Heritage - Ireland's Breathtaking Landscapes</h2>
            <p style="text-align: center; font-size: 1.3em; margin-bottom: 40px; color: #2d5016;">
                Discover the wild beauty of the Emerald Isle, where dramatic cliffs meet endless green fields!
            </p>
            
            <div class="grid">
                <div class="card">
                    <div class="image-placeholder">Cliffs of Moher View</div>
                    <h3>🌊 Cliffs of Moher</h3>
                    <p>Stand 214 meters above the Atlantic Ocean on Ireland's most famous cliffs. These incredible rock formations stretch for 8 kilometers and offer stunning views that will take your breath away. Perfect for amazing photos!</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Giant's Causeway Stones</div>
                    <h3>🗿 Giant's Causeway</h3>
                    <p>Walk on 40,000 magical hexagonal stone columns created by ancient volcanic activity. This UNESCO World Heritage site looks like a giant's stepping stones across the sea. Legend says it was built by the Irish giant Finn McCool!</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Ring of Kerry Landscape</div>
                    <h3>💍 Ring of Kerry</h3>
                    <p>Drive through 179 kilometers of the most beautiful scenery in Ireland. See sparkling lakes, purple mountains, golden beaches, and charming villages. This scenic route is perfect for nature lovers and photographers.</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Killarney National Park</div>
                    <h3>🦌 Killarney National Park</h3>
                    <p>Explore Ireland's first national park with ancient oak forests, crystal-clear lakes, and majestic mountains. Spot red deer, rare birds, and enjoy peaceful boat rides on the famous Lakes of Killarney.</p>
                </div>
            </div>
        </section>

        <section id="cultural">
            <h2>🎭 Cultural Heritage - The Soul of Ireland</h2>
            <p style="text-align: center; font-size: 1.3em; margin-bottom: 40px; color: #2d5016;">
                Experience the rich culture that has given the world amazing literature, music, and art!
            </p>
            
            <div class="grid">
                <div class="card">
                    <div class="image-placeholder">Book of Kells Display</div>
                    <h3>📚 Literature & Libraries</h3>
                    <p><strong>Trinity College Library:</strong> See the famous Book of Kells, a 1,200-year-old illuminated manuscript. Walk through the stunning Long Room with 200,000 ancient books.</p>
                    <p><strong>Writers Museum:</strong> Learn about famous Irish writers like James Joyce, Oscar Wilde, and Bram Stoker (who wrote Dracula!)</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Traditional Irish Music</div>
                    <h3>🎵 Traditional Music</h3>
                    <p><strong>Temple Bar Sessions:</strong> Listen to live traditional Irish music in Dublin's cultural quarter. Hear the fiddle, bodhrán drum, and tin whistle.</p>
                    <p><strong>Doolin Village:</strong> Visit the "music capital" of Ireland where musicians gather every night in cozy pubs for amazing sessions.</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Irish Festivals</div>
                    <h3>🎪 Festivals & Celebrations</h3>
                    <p><strong>St. Patrick's Day:</strong> Join the biggest celebration in the world on March 17th with parades, music, and lots of green!</p>
                    <p><strong>Fleadh Cheoil:</strong> The largest traditional music festival with competitions, workshops, and street performances.</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Ancient Monuments</div>
                    <h3>🏛️ Ancient Monuments</h3>
                    <p><strong>Newgrange:</strong> Visit this 5,000-year-old tomb (older than Stonehenge!) that lights up during winter solstice.</p>
                    <p><strong>Skellig Michael:</strong> Explore the ancient monastery on this rocky island where monks lived 1,400 years ago.</p>
                </div>
            </div>
        </section>

        <section id="traditions">
            <h2>🍀 Irish Traditions - What Makes Ireland Special</h2>
            <p style="text-align: center; font-size: 1.3em; margin-bottom: 40px; color: #2d5016;">
                Discover the unique customs and traditions that make Ireland truly magical!
            </p>
            
            <div class="grid">
                <div class="card">
                    <div class="image-placeholder">Irish Dance Performance</div>
                    <h3>💃 Irish Dancing</h3>
                    <p>Watch amazing Irish step dancing with quick foot movements and beautiful costumes. Learn some basic steps yourself! The most famous show is "Riverdance" which has traveled all over the world.</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Gaelic Sports</div>
                    <h3>🏐 Gaelic Sports</h3>
                    <p><strong>Hurling:</strong> The world's fastest field sport played with wooden sticks and a small ball.</p>
                    <p><strong>Gaelic Football:</strong> A mix of soccer and rugby that's uniquely Irish. Visit Croke Park stadium to watch a match!</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Irish Language Signs</div>
                    <h3>🗣️ Irish Language (Gaeilge)</h3>
                    <p>Learn basic Irish phrases! "Céad míle fáilte" means "one hundred thousand welcomes." Visit the Gaeltacht regions where Irish is still spoken daily, especially in western Ireland.</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Traditional Irish Food</div>
                    <h3>🍲 Traditional Food</h3>
                    <p><strong>Irish Stew:</strong> Hearty lamb and potato stew perfect for cold days.</p>
                    <p><strong>Soda Bread:</strong> Fresh bread made without yeast, served warm with butter.</p>
                    <p><strong>Fish & Chips:</strong> Fresh fish from Irish waters with crispy chips!</p>
                </div>
            </div>
        </section>

        <section id="screen">
            <h2>🎬 Screen Tourism - Famous Filming Locations</h2>
            <p style="text-align: center; font-size: 1.3em; margin-bottom: 40px; color: #2d5016;">
                Visit the magical places where your favorite movies and TV shows were filmed!
            </p>
            
            <div class="grid">
                <div class="card">
                    <div class="image-placeholder">Star Wars Skellig Michael</div>
                    <h3>⭐ Star Wars: The Last Jedi</h3>
                    <p><strong>Skellig Michael:</strong> This dramatic island off the Kerry coast was Luke Skywalker's hiding place. Take a boat trip to see where the final scenes were filmed. The ancient monastery adds to the mystical atmosphere!</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Game of Thrones Locations</div>
                    <h3>🐉 Game of Thrones</h3>
                    <p><strong>Northern Ireland:</strong> Visit the real-life Winterfell at Castle Ward, walk through the Dark Hedges (Kingsroad), and see the Giant's Causeway (Dragonstone beaches). Take the official Game of Thrones tour!</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Harry Potter Scenes</div>
                    <h3>⚡ Harry Potter Films</h3>
                    <p><strong>Cliffs of Moher:</strong> These cliffs appeared as the dramatic backdrop in "Harry Potter and the Half-Blood Prince" when Harry and Dumbledore visit the sea cave. Feel the magic yourself!</p>
                </div>
                
                <div class="card">
                    <div class="image-placeholder">Normal People Locations</div>
                    <h3>💕 Normal People</h3>
                    <p><strong>Trinity College Dublin & County Sligo:</strong> Follow Marianne and Connell's story through the beautiful college campus and the stunning western coastline where they spent their summer.</p>
                </div>
            </div>
        </section>

        <div class="road-trip" id="roadtrip">
            <h2 style="color: white;">🚗 Ultimate Ireland Road Trip - 7 Days Itinerary</h2>
            <p style="text-align: center; font-size: 1.3em; margin-bottom: 40px;">
                Follow this amazing route to see the best of Ireland in one week!
            </p>
            
            <div class="itinerary">
                <div class="day">
                    <h4>Day 1: Dublin - The Capital Adventure</h4>
                    <p><strong>Morning:</strong> Start at Trinity College, see the Book of Kells</p>
                    <p><strong>Afternoon:</strong> Walk through Temple Bar, visit Dublin Castle</p>
                    <p><strong>Evening:</strong> Enjoy traditional music and Irish stew in a cozy pub</p>
                    <p><strong>Distance:</strong> Walking day in city center</p>
                </div>
                
                <div class="day">
                    <h4>Day 2: Dublin to Kilkenny (127 km - 1.5 hours)</h4>
                    <p><strong>Morning:</strong> Drive south to medieval Kilkenny</p>
                    <p><strong>Afternoon:</strong> Explore Kilkenny Castle and medieval streets</p>
                    <p><strong>Evening:</strong> Try local craft beer and traditional Irish music</p>
                </div>
                
                <div class="day">
                    <h4>Day 3: Kilkenny to Cork (162 km - 2 hours)</h4>
                    <p><strong>Morning:</strong> Drive to Cork, Ireland's second largest city</p>
                    <p><strong>Afternoon:</strong> Visit the famous English Market, kiss the Blarney Stone</p>
                    <p><strong>Evening:</strong> Explore Cork's vibrant nightlife and restaurants</p>
                </div>
                
                <div class="day">
                    <h4>Day 4: Cork to Killarney (87 km - 1 hour)</h4>
                    <p><strong>Morning:</strong> Drive to beautiful Killarney</p>
                    <p><strong>Afternoon:</strong> Explore Killarney National Park, take a boat on the lakes</p>
                    <p><strong>Evening:</strong> Traditional Irish music session in town</p>
                </div>
                
                <div class="day">
                    <h4>Day 5: Ring of Kerry (179 km circular route)</h4>
                    <p><strong>Full Day:</strong> Drive the famous Ring of Kerry scenic route</p>
                    <p><strong>Stops:</strong> Kenmare, Sneem, Waterville, Cahersiveen</p>
                    <p><strong>Highlights:</strong> Stunning mountain and ocean views, charming villages</p>
                    <p><strong>Evening:</strong> Return to Killarney</p>
                </div>
                
                <div class="day">
                    <h4>Day 6: Killarney to Cliffs of Moher (155 km - 2 hours)</h4>
                    <p><strong>Morning:</strong> Drive north through County Clare</p>
                    <p><strong>Afternoon:</strong> Visit the spectacular Cliffs of Moher</p>
                    <p><strong>Evening:</strong> Stay in nearby Doolin village for traditional music</p>
                </div>
                
                <div class="day">
                    <h4>Day 7: Cliffs of Moher to Dublin (268 km - 3 hours)</h4>
                    <p><strong>Morning:</strong> Final views of the cliffs, visit Doolin</p>
                    <p><strong>Afternoon:</strong> Drive back to Dublin with stops in charming villages</p>
                    <p><strong>Evening:</strong> Farewell dinner in Dublin with traditional Irish entertainment</p>
                </div>
            </div>
            
            <div style="background: rgba(255,255,255,0.1); padding: 30px; border-radius: 15px; margin-top: 40px;">
                <h3 style="color: #90EE90; margin-bottom: 20px;">🎒 Essential Road Trip Tips:</h3>
                <ul style="list-style: none; line-height: 2;">
                    <li>🚗 <strong>Car Rental:</strong> Book early, remember to drive on the left!</li>
                    <li>🏨 <strong>Accommodation:</strong> Book B&Bs and hotels in advance</li>
                    <li>📱 <strong>Apps:</strong> Download offline maps and weather apps</li>
                    <li>☔ <strong>Weather:</strong> Pack waterproof clothes (it's Ireland!)</li>
                    <li>💶 <strong>Budget:</strong> About €100-150 per day including accommodation</li>
                    <li>📷 <strong>Camera:</strong> Bring extra batteries for all those amazing photos!</li>
                </ul>
            </div>
        </div>

        <div class="cta">
            <h2 style="color: white; margin-bottom: 20px;">Ready for Your Irish Adventure?</h2>
            <p style="font-size: 1.3em; margin-bottom: 30px;">
                Don't just dream about it - make it happen! Ireland is waiting for you with open arms and endless stories to tell.
            </p>
            <a href="#" class="cta-button">Start Planning Your Trip Now!</a>
        </div>
    </div>

    <footer>
        <div class="container">
            <p>&copy; 2025 Discover Ireland. Made with 💚 for travelers who love adventure!</p>
            <p style="margin-top: 10px; font-style: italic;">
                "May the road rise up to meet you, and the wind be always at your back" - Traditional Irish Blessing
            </p>
        </div>
    </footer>

    <script>
        // Simple smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        window.addEventListener('scroll', () => {
            const cards = document.querySelectorAll('.card');
            cards.forEach(card => {
                const cardTop = card.getBoundingClientRect().top;
                if (cardTop < window.innerHeight - 100) {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }
            });
        });

        // Initialize card animation
        document.addEventListener('DOMContentLoaded', () => {
            const cards = document.querySelectorAll('.card');
            cards.forEach((card, index) => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(50px)';
                card.style.transition = 'all 0.6s ease';
                card.style.transitionDelay = `${index * 0.1}s`;
            });
        });
    </script>
</body>
</html>