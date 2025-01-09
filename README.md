<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galeria de Fotos</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <style>
        body {
            font-family: "Georgia", serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            background-color: #f4f4f4;
            color: #333;
        }

        header {
            background: url('https://via.placeholder.com/1920x400') center/cover no-repeat;
            color: #f4f4f4;
            text-align: center;
            padding: 5rem 1rem;
            position: relative;
        }

        header h1 {
            font-size: 3.5rem;
            margin: 0;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
            color: #2a3b3c;
        }

        .search-bar {
            padding: 10px 20px;
            font-size: 1rem;
            border: 2px solid #2a3b3c;
            border-radius: 25px;
            background-color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 1.5rem auto;
            max-width: 400px;
        }

        .search-bar input {
            border: none;
            outline: none;
            padding: 5px;
            font-size: 1rem;
            background: transparent;
            color: #333;
            flex: 1;
        }

        .search-bar i {
            margin-left: 10px;
            font-size: 1.5rem;
            color: #2a3b3c;
            cursor: pointer;
        }

        .section {
            padding: 6rem 1.5rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: #2a3b3c;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .section-subtitle {
            text-align: center;
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: #666;
            font-style: italic;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
            padding: 0 2rem;
        }

        .gallery img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .features {
            display: flex;
            justify-content: center;
            gap: 2rem;
            padding: 2rem;
            flex-wrap: wrap;
        }

        .feature {
            background-color: #eae4df;
            border-radius: 10px;
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
            width: 250px;
        }

        .feature:hover {
            transform: scale(1.05);
        }

        .feature h3 {
            font-size: 1.5rem;
            color: #2a3b3c;
            margin-bottom: 1rem;
        }

        .feature p {
            font-size: 1rem;
            color: #666;
            margin-bottom: 1rem;
        }

        .about {
            background-color: #2a3b3c;
            color: #f4f4f4;
            display: flex;
            flex-wrap: wrap;
            padding: 6rem 1rem;
            gap: 2rem;
            align-items: center;
            justify-content: center;
        }

        .about-text {
            flex: 1 1 50%;
            padding: 1rem;
            text-align: center;
        }

        .about-text h2 {
            font-size: 2.5rem;
            color: #e1d9d1;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .about-text p {
            font-size: 1.2rem;
            line-height: 1.6;
        }

        footer {
            text-align: center;
            padding: 3rem 0;
            background-color: #2a3b3c;
            color: #e1d9d1;
            border-top: 4px solid #d9cdc3;
            font-size: 1rem;
        }

        footer p {
            margin: 0;
        }

        .gallery-section {
            background-color: #f0f0f0;
            padding: 4rem 1.5rem;
        }

        .copyright {
            font-size: 0.8rem;
            color: #666;
            margin-top: 10px;
        }

        .no-results {
            font-size: 1.2rem;
            color: #777;
            text-align: center;
            margin-top: 2rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>Galeria de Fotos</h1>
    </header>

    <section class="about">
        <div class="about-text">
            <h2>Descubra a Nossa Galeria</h2>
            <p>Bem-vindo à nossa Galeria de Fotos! Aqui, você encontra um lugar para relaxar, se inspirar e explorar diversas imagens. Cada foto foi cuidadosamente selecionada para lhe proporcionar uma experiência visual única. Navegue à vontade e descubra coleções fascinantes que vão de paisagens deslumbrantes a momentos especiais capturados de forma simples e verdadeira.</p>
        </div>

        <div class="features">
            <div class="feature">
                <h3>Exibição Simples e Organizada</h3>
                <p>Na nossa galeria, cada imagem é apresentada de forma clara e acessível. O layout em grade facilita a navegação, permitindo que você explore rapidamente e se maravilhe com cada detalhe das fotos.</p>
            </div>
            <div class="feature">
                <h3>Encontre o que Procura</h3>
                <p>Use nossa barra de busca para encontrar exatamente o que você deseja! Pesquise por palavras-chave e veja os resultados em tempo real, tornando a experiência ainda mais prática e agradável.</p>
            </div>
        </div>
    </section>

    <section class="gallery-section">
        <h2 class="section-title">Explore Nossa Coleção</h2>
        <p class="section-subtitle">Em nossa galeria, você pode se perder por horas explorando imagens de todos os tipos. Cada uma delas conta uma história.</p>

        <div class="search-bar">
            <input type="text" id="search" placeholder="Encontre a foto que você procura..." onkeyup="fetchPhotosByCategoryFromPexels(this.value)">
            <i class="fas fa-search" onclick="searchByClick()"></i>
        </div>

        <div class="gallery" id="gallery"></div>
        <p id="no-results" class="no-results" style="display:none;">Nenhuma foto encontrada.</p>
    </section>

    <footer>
        <h2>Obrigado por visitar nossa galeria!</h2>
        <p>Continuamos trazendo imagens incríveis para você. Fique de olho para mais novidades e inspirações.</p>
    </footer>

    <script>
        const API_KEY = 'vOGdCUs2Og4025EsCp4wOfDBdAtq2RKR9Aoms3l12NMtFxsAhT6IDGI4';

        const categoriesInPortuguese = {
            'nature': 'natureza',
            'city': 'cidade',
            'business': 'negócios',
            'travel': 'viagem',
            'people': 'pessoas',
            'animals': 'animais',
            'technology': 'tecnologia',
            'fashion': 'moda',
            'sports': 'esportes',
            'food': 'comida',
            'architecture': 'arquitetura'
        };

        const imageNamesInPortuguese = {
            'accusamus beatae ad facilis cum similique qui sunt': 'Beleza do campo',
            'aliquam amet autem iure quam doloribus': 'Beleza das montanhas',
            'autem harum iusto': 'Paisagens deslumbrantes',
            'et rerum tempore vitae': 'Reflexão tranquila',
            'exercitationem commodi': 'Escapando para a natureza',
            'in quis et ea': 'Vista serena do mar',
            'officia porro iure quia iusto qui ipsa ut modi': 'Paisagem urbana com montanhas',
            'sit sunt voluptatibus': 'Beleza da primavera',
            'suscipit laboriosam, nisi ut aliquip ex ea commodo consequat': 'Cores da estação',
            'voluptates optio qui nihil at': 'Cenário paradisíaco'
        };

        async function fetchPhotosFromPexels() {
            const URL = 'https://api.pexels.com/v1/curated?per_page=20';
            emptyGalleryDiv();

            try {
                const response = await fetch(URL, {
                    headers: {
                        Authorization: API_KEY,
                    },
                });
                const data = await response.json();
                displayPhotos(data.photos);
            } catch (error) {
                console.error('Erro ao carregar fotos do Pexels:', error);
            }
        }

        async function fetchPhotosByCategoryFromPexels(category) {
            const translatedCategory = categoriesInPortuguese[category.toLowerCase()] || category.toLowerCase();
            const URL = `https://api.pexels.com/v1/search?query=${translatedCategory}&per_page=20`;
            emptyGalleryDiv();

            try {
                const response = await fetch(URL, {
                    headers: {
                        Authorization: API_KEY,
                    },
                });
                const data = await response.json();
                displayPhotos(data.photos);
            } catch (error) {
                console.error('Erro ao carregar fotos do Pexels:', error);
            }
        }

        function searchByClick() {
            const searchInput = document.getElementById('search');
            fetchPhotosByCategoryFromPexels(searchInput.value);
        }

        function emptyGalleryDiv() {
            const gallery = document.getElementById('gallery');
            gallery.innerHTML = ''; 
            document.getElementById('no-results').style.display = 'none';
        }

        function displayPhotos(photos) {
            emptyGalleryDiv();

            if (photos.length === 0) {
                document.getElementById('no-results').style.display = 'block';
            } else {
                photos.forEach(photo => {
                    const photoElement = document.createElement('div');
                    photoElement.style.textAlign = 'center';
                    photoElement.style.marginBottom = '20px';

                    const placeholder = document.createElement('div');
                    placeholder.classList.add('placeholder');
                    placeholder.textContent = 'Carregando...';

                    const img = document.createElement('img');
                    img.alt = photo.alt;

                    img.onload = () => {
                        placeholder.style.display = "none";
                        img.style.display = "block";
                    };

                    img.src = photo.src.landscape;

                    const title = document.createElement('p');
                    const translatedTitle = imageNamesInPortuguese[photo.alt] || photo.alt;
                    title.textContent = translatedTitle;
                    title.style.marginTop = '10px';
                    title.style.fontSize = '0.9rem';
                    title.style.color = '#333';

                    const copyright = document.createElement('p');
                    const photoYear = photo.created_at ? new Date(photo.created_at).getFullYear() : new Date().getFullYear();
                    copyright.textContent = `© ${photoYear} Galeria de Fotos. Todos os direitos reservados.`;
                    copyright.classList.add('copyright');
                    copyright.style.marginTop = '5px';
                    copyright.style.fontSize = '0.8rem';
                    copyright.style.color = '#666';

                    photoElement.appendChild(placeholder);
                    photoElement.appendChild(img);
                    photoElement.appendChild(title);
                    photoElement.appendChild(copyright);
                    gallery.appendChild(photoElement);
                });
            }
        }

        fetchPhotosFromPexels();
    </script>
</body>
</html>
