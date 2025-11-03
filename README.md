<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Coffee Break Collection | Löfbergs</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        :root {
            --primary: #3a225d; /* Löfbergs purple */
            --secondary: #d4af37; /* Gold accent */
            --accent: #e8d7f1; /* Light purple */
            --light: #f9f6fb; /* Very light purple */
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--primary);
            overflow-x: hidden;
        }
        
        .title {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }
        
        .card {
            background: white;
            box-shadow: 0 10px 30px rgba(43, 58, 85, 0.1);
            transform-style: preserve-3d;
            transition: all 0.5s ease;
        }
        
        .card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 15px 35px rgba(43, 58, 85, 0.2);
        }
        
        .btn {
            background: var(--secondary);
            transition: all 0.3s ease;
            transform: translateY(0);
        }
        
        .btn:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .btn:active {
            transform: translateY(1px);
        }
        
        .hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 10;
        }
        
        .heart {
            position: absolute;
            font-size: 1.5rem;
            color: var(--secondary);
            animation: float 4s ease-in-out infinite;
            opacity: 0;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(20deg);
                opacity: 0;
            }
        }
        
        .fika-icon {
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
        }
        
        .flag {
            width: 80px;
            height: 60px;
            background: linear-gradient(
                to bottom,
                #006AA7 0%, #006AA7 30%,
                #FECC02 30%, #FECC02 40%,
                #006AA7 40%, #006AA7 70%,
                #FECC02 70%, #FECC02 80%,
                #006AA7 80%, #006AA7 100%
            );
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .hygge {
            background: radial-gradient(circle, var(--accent) 0%, var(--light) 70%);
        }
    </style>
</head>
<body class="min-h-screen bg-gradient-to-b from-var(--light) to-white">
    <!-- Hero Section -->
    <section class="relative min-h-[80vh] flex items-center justify-center bg-[url('https://drive.google.com/uc?export=view&id=1-WCsZw9Wi6aXZSshZd6SJGVUc7o00A9Q')] bg-cover bg-center">
        <div class="absolute inset-0 bg-black bg-opacity-30"></div>
        <div class="relative z-10 text-center px-4 max-w-4xl mx-auto">
            <img src="lofbergs-logo.png" alt="Löfbergs" class="h-16 mx-auto mb-8">
            <h1 class="title text-5xl md:text-6xl text-white mb-4">The Coffee Break Collection</h1>
            <p class="text-xl text-white mb-8">Take a Break, Play Together</p>
            <a href="#games" class="btn bg-var(--secondary) hover:bg-var(--primary) text-white py-3 px-8 rounded-full text-lg font-medium transition-all">
                Explore the Games
            </a>
        </div>
    </section>

    <!-- Product Grid -->
    <section id="games" class="py-16 px-4 max-w-6xl mx-auto">
        <h2 class="title text-3xl text-center mb-12">Our Coffee Break Games</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Game 1 -->
            <div class="card rounded-xl p-6 bg-white shadow-lg hover:shadow-xl transition-shadow">
                <img src="https://drive.google.com/uc?export=view&id=19lmFC5hkBpGDrsAqVazPaJc60v0w790W" alt="Brew Battle" class="w-full h-48 object-contain mb-4">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="text-xl font-bold">Brew Battle</h3>
                    <img src="lofbergs-logo-small.png" alt="Löfbergs" class="h-6">
                </div>
                <p class="text-gray-600 mb-4">A fast-paced coffee trivia game for the office break room.</p>
                <button class="btn w-full bg-var(--primary) hover:bg-var(--secondary) text-white py-2 rounded-lg">
                    Add to Cart
                </button>
            </div>

            <!-- Game 2 -->
            <div class="card rounded-xl p-6 bg-white shadow-lg hover:shadow-xl transition-shadow">
                <img src="https://drive.google.com/uc?export=view&id=19lmFC5hkBpGDrsAqVazPaJc60v0w790W" alt="Bean Bingo" class="w-full h-48 object-contain mb-4">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="text-xl font-bold">Bean Bingo</h3>
                    <img src="lofbergs-logo-small.png" alt="Löfbergs" class="h-6">
                </div>
                <p class="text-gray-600 mb-4">Match coffee flavors and roast profiles in this aromatic bingo game.</p>
                <button class="btn w-full bg-var(--primary) hover:bg-var(--secondary) text-white py-2 rounded-lg">
                    Add to Cart
                </button>
            </div>

            <!-- Game 3 -->
            <div class="card rounded-xl p-6 bg-white shadow-lg hover:shadow-xl transition-shadow">
                <img src="https://drive.google.com/uc?export=view&id=19lmFC5hkBpGDrsAqVazPaJc60v0w790W" alt="Espresso Escape" class="w-full h-48 object-contain mb-4">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="text-xl font-bold">Espresso Escape</h3>
                    <img src="lofbergs-logo-small.png" alt="Löfbergs" class="h-6">
                </div>
                <p class="text-gray-600 mb-4">A cooperative puzzle game perfect for your 15-minute break.</p>
                <button class="btn w-full bg-var(--primary) hover:bg-var(--secondary) text-white py-2 rounded-lg">
                    Add to Cart
                </button>
            </div>
        </div>
    </section>
    
    <script>
        // Simple hover effect for product cards
        document.querySelectorAll('.card').forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.transform = 'translateY(-5px)';
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'translateY(0)';
            });
        });
    </script>
</body>
</html>
