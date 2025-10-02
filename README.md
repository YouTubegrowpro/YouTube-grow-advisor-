<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="YouTube Vistar Salahkar: AI-powered tools for YouTube creators to optimize SEO, audit channels, generate trending ideas, create scripts, and design thumbnails.">
    <meta name="keywords" content="YouTube growth, SEO, channel audit, trending ideas, thumbnail maker, AI tools">
    <meta name="google-site-verification" content="IBIxq7l1jTl5OYSP1t3NebJUiZ9_neYoZncfr7xwWxE" />
    <meta property="og:title" content="YouTube Vistar Salahkar - Grow Your YouTube Channel">
    <meta property="og:description" content="Boost your YouTube channel with AI-powered SEO, audits, trending ideas, scripts, and thumbnails.">
    <meta property="og:image" content="https://yourdomain.com/assets/hero-image.jpg">
    <meta name="twitter:card" content="summary_large_image">
    <title>YouTube Vistar Salahkar</title>
    <link href="/css/tailwind.min.css" rel="stylesheet"> <!-- Local Tailwind CSS -->
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800;900&display=swap');
      
      body {
        background-color: #0f0f0f;
        color: #ffffff;
        font-family: 'Inter', sans-serif;
        min-height: 100vh;
      }
      
      .tab-button.active {
        border-bottom: 4px solid #FF0000;
        color: #FF0000;
        font-weight: 700;
        background: linear-gradient(180deg, #1a1a1a, #0f0f0f);
      }
      
      .tab-button:hover {
        background: linear-gradient(180deg, #2a2a2a, #1a1a1a);
        color: #FF4444;
      }
      
      .loader {
        border: 4px solid #f3f3f3;
        border-top: 4px solid #FF0000;
        border-radius: 50%;
        width: 20px;
        height: 20px;
        animation: spin 1s linear infinite;
        margin: 0 auto;
        display: none;
      }
      
      .loading .loader { display: block; }
      .loading .submit-text { display: none; }

      @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
      }

      input[type="text"], textarea, select {
        background-color: #1a1a1a !important;
        border: 1px solid #333333 !important;
        color: #ffffff !important;
        border-radius: 8px !important;
        padding: 10px !important;
      }
      
      .user-id-box {
        background: linear-gradient(45deg, #272727, #333333);
        border: 1px dashed #FF0000;
        padding: 8px 12px;
        border-radius: 8px;
        font-size: 0.8rem;
        color: #FFDDDD;
      }

      .hero-section {
        background: url('https://images.unsplash.com/photo-1611162617474-5b21e879e8b1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
        border-radius: 12px;
        padding: 3rem;
        text-align: center;
        box-shadow: 0 4px 20px rgba(255, 0, 0, 0.2);
      }

      @media (max-width: 640px) {
        .flex.border-b { flex-direction: column; }
        .tab-button { width: 100%; }
      }
    </style>
    <!-- Google Analytics -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-YOUR_TRACKING_ID"></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', 'G-YOUR_TRACKING_ID');
    </script>
</head>
<body>
    <div class="min-h-screen flex flex-col">
      <header class="bg-yt-dark sticky top-0 z-50 shadow-lg border-b border-yt-red/50">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
          <div class="flex items-center space-x-2">
            <svg class="youtube-logo w-6 h-6 fill-yt-red" viewBox="0 0 24 24">
              <path d="M12 0C5.37 0 0 5.37 0 12s5.37 12 12 12 12-5.37 12-12S18.63 0 12 0zm5.79 16.5c-.21.74-.82 1.35-1.56 1.56C14.88 18.5 12 18.5 12 18.5s-2.88 0-4.23-.44c-.74-.21-1.35-.82-1.56-1.56C6 15.12 6 12 6 12s0-3.12.44-4.23c.21-.74.82-1.35 1.56-1.56C9.12 6 12 6 12 6s2.88 0 4.23.44c.74.21 1.35.82 1.56 1.56C18 8.88 18 12 18 12s0 3.12-.44 4.23zM10 14.5v-5l4 2.5z"/>
            </svg>
            <span class="text-xl font-extrabold text-yt-light tracking-tight">YouTube Vistar Salahkar</span>
          </div>
          <div class="flex items-center space-x-4">
            <select id="language-select" class="bg-yt-dark text-yt-light rounded-md p-2 border border-yt-grey text-sm focus:ring-yt-red focus:border-yt-red" aria-label="Select Language">
              <option value="Hindi">🌐 हिंदी</option>
              <option value="English">🇬🇧 English</option>
              <option value="Spanish">🇪🇸 Español</option>
              <option value="French">🇫🇷 Français</option>
              <option value="Japanese">🇯🇵 日本語</option>
            </select>
            <div class="user-id-box">
              User ID: <span id="user-id">Loading...</span>
            </div>
          </div>
        </div>
      </header>

      <section class="hero-section mb-6">
        <h1 class="text-4xl font-bold text-yt-light mb-4">Grow Your YouTube Channel with AI</h1>
        <p class="text-lg text-yt-light mb-6">Optimize SEO, audit channels, find trending ideas, write scripts, and create stunning thumbnails.</p>
        <button class="bg-yt-red text-yt-light font-bold py-3 px-6 rounded-xl hover:bg-red-700 transition duration-300" onclick="document.getElementById('video-seo').scrollIntoView()">Get Started</button>
      </section>

      <main class="flex-grow max-w-7xl mx-auto w-full px-4 sm:px-6 lg:px-8 py-6">
        <div class="flex border-b border-yt-grey overflow-x-auto whitespace-nowrap mb-6">
          <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300 active" data-tab="video-seo" aria-label="Video SEO Tab">🎬 वीडियो SEO</button>
          <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="channel-audit" aria-label="Channel Audit Tab">📈 चैनल समीक्षा</button>
          <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="trending-ideas" aria-label="Trending Ideas Tab">🔥 ट्रेंडिंग विचार</button>
          <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="script-story" aria-label="Script and Story Tab">✍️ स्क्रिप्ट / स्टोरी</button>
          <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="thumbnail-maker" aria-label="Thumbnail Maker Tab">🖼️ थंबनेल मेकर</button>
        </div>
        
        <div class="w-full mb-6 mt-4">
          <div class="bg-yt-med-grey p-3 rounded-xl border border-yt-grey text-center shadow-lg">
            <p class="text-xs font-semibold text-gray-400 mb-2 uppercase tracking-wider">Advertisement / प्रायोजक</p>
            <div id="top-banner-ad" class="w-full bg-yt-dark py-4 rounded-lg flex items-center justify-center min-h-[90px]">
              <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-1234567890123456" crossorigin="anonymous"></script>
              <ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-1234567890123456" data-ad-slot="1234567890" data-ad-format="auto"></ins>
              <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
            </div>
          </div>
        </div>
        
        <div id="tab-content">
          <div id="video-seo" class="tab-pane active space-y-6">
            <h2 class="text-2xl font-bold text-yt-red">🎬 वीडियो SEO</h2>
            <input type="text" id="seo-topic" placeholder="आपके वीडियो का मुख्य विषय क्या है? (जैसे: ब्लॉग्गिंग से पैसे कैसे कमाएं)" class="w-full" aria-label="Video Topic Input">
            <button onclick="handleVideoOptimization('video-seo-output', 'seo-topic')" 
                    class="w-full bg-yt-red text-yt-light font-bold py-3 rounded-xl shadow-lg hover:bg-red-700 transition duration-300 flex items-center justify-center relative">
              <span class="submit-text">SEO सामग्री जनरेट करें</span>
              <div class="loader" id="seo-loader"></div>
            </button>
            <div id="video-seo-output" class="bg-yt-med-grey p-4 rounded-xl shadow-inner border border-yt-grey min-h-[150px] text-sm whitespace-pre-wrap">
              <p class="text-gray-400">यहां शीर्षक, विवरण, टैग और वायरल वीडियो लिंक दिखाई देंगे।</p>
            </div>
          </div>

          <div id="channel-audit" class="tab-pane hidden space-y-6">
            <h2 class="text-2xl font-bold text-yt-red">📈 चैनल समीक्षा (Audit)</h2>
            <input type="text" id="audit-link" placeholder="अपने YouTube चैनल या वीडियो का लिंक पेस्ट करें (उदा: https://youtube.com/@TechChannel)" class="w-full" aria-label="Channel Link Input">
            <button onclick="handleChannelAudit('audit-output', 'audit-link')"
                    class="w-full bg-yt-red text-yt-light font-bold py-3 rounded-xl shadow-lg hover:bg-red-700 transition duration-300 flex items-center justify-center relative">
              <span class="submit-text">AI से चैनल ऑडिट कराएँ</span>
              <div class="loader" id="audit-loader"></div>
            </button>
            <div id="audit-output" class="bg-yt-med-grey p-4 rounded-xl shadow-inner border border-yt-grey min-h-[150px] text-sm whitespace-pre-wrap">
              <p class="text-gray-400">यहां AI-आधारित समीक्षा, सुधार के सुझाव, और 'क्या कमी है' का विवरण दिखाई देगा।</p>
            </div>
          </div>
          
          <div id="trending-ideas" class="tab-pane hidden space-y-6">
            <h2 class="text-2xl font-bold text-yt-red">🔥 ट्रेंडिंग विचार</h2>
            <input type="text" id="trend-niche" placeholder="अपने चैनल की श्रेणी या Niche डालें (उदा: टेक्नोलॉजी, कुकिंग, फाइनेंस)" class="w-full" aria-label="Niche Input">
            <button onclick="handleTrendGeneration('trend-output', 'trend-niche')"
                    class="w-full bg-yt-red text-yt-light font-bold py-3 rounded-xl shadow-lg hover:bg-red-700 transition duration-300 flex items-center justify-center relative">
              <span class="submit-text">5 ट्रेंडिंग विचार खोजें</span>
              <div class="loader" id="trend-loader"></div>
            </button>
            <div id="trend-output" class="bg-yt-med-grey p-4 rounded-xl shadow-inner border border-yt-grey min-h-[150px] text-sm whitespace-pre-wrap">
              <p class="text-gray-400">यहां आपके Niche से संबंधित वायरल वीडियो विचार दिखाई देंगे।</p>
            </div>
          </div>

          <div id="script-story" class="tab-pane hidden space-y-6">
            <h2 class="text-2xl font-bold text-yt-red">✍️ स्क्रिप्ट और स्टोरी</h2>
            <input type="text" id="script-topic" placeholder="आपके वीडियो का विषय (उदा: इतिहास का सबसे बड़ा रहस्य)" class="w-full" aria-label="Script Topic Input">
            <select id="script-style" class="w-full bg-yt-dark text-yt-light rounded-md p-3 border border-yt-grey focus:ring-yt-red focus:border-yt-red" aria-label="Script Style Selector">
              <option value="Informative and Educational">जानकारीपूर्ण और शैक्षिक</option>
              <option value="Review and Critical Analysis">समीक्षा और गहन विश्लेषण</option>
              <option value="Storytelling and Historical">कहानी सुनाना और ऐतिहासिक</option>
              <option value="Step-by-step Tutorial">स्टेप-बाय-स्टेप ट्यूटोरियल</option>
            </select>
            <button onclick="handleScriptGeneration('script-output', 'script-topic', 'script-style')"
                    class="w-full bg-yt-red text-yt-light font-bold py-3 rounded-xl shadow-lg hover:bg-red-700 transition duration-300 flex items-center justify-center relative">
              <span class="submit-text">स्क्रिप्ट और स्टोरी जनरेट करें</span>
              <div class="loader" id="script-loader"></div>
            </button>
            <div id="script-output" class="bg-yt-med-grey p-4 rounded-xl shadow-inner border border-yt-grey min-h-[150px] text-sm whitespace-pre-wrap">
              <p class="text-gray-400">यहां विस्तृत वीडियो स्क्रिप्ट और आकर्षक कहानी के विचार दिखाई देंगे।</p>
            </div>
          </div>

          <div id="thumbnail-maker" class="tab-pane hidden space-y-6">
            <h2 class="text-2xl font-bold text-yt-red">🖼️ थंबनेल मेकर</h2>
            <textarea id="thumbnail-prompt" rows="3" placeholder="थंबनेल का विस्तृत विवरण दें (उदा: एक हैरान आदमी ₹1 लाख के नोट पकड़े हुए, टेक्स्ट 'HOW I EARNED IT' बड़े अक्षरों में)" class="w-full" aria-label="Thumbnail Prompt Input"></textarea>
            <button onclick="handleThumbnailGeneration('thumbnail-output', 'thumbnail-prompt')"
                    class="w-full bg-yt-red text-yt-light font-bold py-3 rounded-xl shadow-lg hover:bg-red-700 transition duration-300 flex items-center justify-center relative">
              <span class="submit-text">थंबनेल जनरेट करें</span>
              <div class="loader" id="thumbnail-loader"></div>
            </button>
            <div id="thumbnail-output" class="bg-yt-med-grey p-4 rounded-xl shadow-inner border border-yt-grey min-h-[250px] flex items-center justify-center">
              <p class="text-gray-400">यहां आपका AI-जनरेटेड थंबनेल दिखाई देगा।</p>
            </div>
          </div>
        </div>
      </main>

      <footer class="bg-yt-dark py-4 text-center text-gray-500 text-sm border-t border-yt-grey">
        <p>Powered by Gemini AI, Imagen 3.0, and YouTube Data API. Designed for YouTube Creators.</p>
        <p>&copy; 2025 YouTube Vistar Salahkar. All Rights Reserved.</p>
      </footer>
    </div>

    <script src="https://apis.google.com/js/api.js"></script>
    <script>
      // Language Translations
      const translations = {
        Hindi: {
          seoButton: "SEO सामग्री जनरेट करें",
          seoPlaceholder: "आपके वीडियो का मुख्य विषय क्या है? (जैसे: ब्लॉग्गिंग से पैसे कैसे कमाएं)",
          auditButton: "AI से चैनल ऑडिट कराएँ",
          auditPlaceholder: "अपने YouTube चैनल या वीडियो का लिंक पेस्ट करें (उदा: https://youtube.com/@TechChannel)",
          trendButton: "5 ट्रेंडिंग विचार खोजें",
          trendPlaceholder: "अपने चैनल की श्रेणी या Niche डालें (उदा: टेक्नोलॉजी, कुकिंग, फाइनेंस)",
          scriptButton: "स्क्रिप्ट और स्टोरी जनरेट करें",
          scriptPlaceholder: "आपके वीडियो का विषय (उदा: इतिहास का सबसे बड़ा रहस्य)",
          thumbnailButton: "थंबनेल जनरेट करें",
          thumbnailPlaceholder: "थंबनेल का विस्तृत विवरण दें (उदा: एक हैरान आदमी ₹1 लाख के नोट पकड़े हुए, टेक्स्ट 'HOW I EARNED IT' बड़े अक्षरों में)"
        },
        English: {
          seoButton: "Generate SEO Content",
          seoPlaceholder: "What's your video's main topic? (e.g., How to earn money from blogging)",
          auditButton: "Audit Channel with AI",
          auditPlaceholder: "Paste your YouTube channel or video link (e.g., https://youtube.com/@TechChannel)",
          trendButton: "Find 5 Trending Ideas",
          trendPlaceholder: "Enter your channel's niche (e.g., Technology, Cooking, Finance)",
          scriptButton: "Generate Script & Story",
          scriptPlaceholder: "Your video topic (e.g., The greatest mystery in history)",
          thumbnailButton: "Generate Thumbnail",
          thumbnailPlaceholder: "Describe the thumbnail in detail (e.g., A shocked man holding ₹1 lakh notes, text 'HOW I EARNED IT' in bold)"
        }
        // Add more languages (Spanish, French, Japanese) as needed
      };

      // Global Setup
      const GEMINI_MODEL = "gemini-1.5-pro"; // Stable model
      const IMAGEN_MODEL = "imagen-3.0-generate-002";
      const YOUTUBE_API_KEY = "AIzaSyAWnrW0FhLzKgqJsZ0WNjbyvfFv1jrxSb0"; // YouTube API key
      const GEMINI_API_KEY = "AIzaSyCOVBfEQfsAMD010Tg09nH4MKzpzf1F72w"; // New Gemini API key
      let userId = 'USER-' + (crypto.randomUUID ? crypto.randomUUID() : Math.random().toString(36).substring(2, 9));

      function setUserIdDisplay() {
        document.getElementById('user-id').textContent = userId;
      }

      // Initialize YouTube API
      function initYouTubeAPI() {
        gapi.load('client', () => {
          gapi.client.setApiKey(YOUTUBE_API_KEY);
          gapi.client.load('youtube', 'v3', () => {
            console.log('YouTube API loaded!');
          });
        });
      }

      // API Call Utility
      function callAPI(url, payload, isImage = false) {
        return new Promise((resolve, reject) => {
          if (!GEMINI_API_KEY || GEMINI_API_KEY === "YOUR_GEMINI_API_KEY") {
            return reject(new Error('Gemini API Key Missing: कृपया कोड में अपनी API Key डालें।'));
          }
          
          const xhr = new XMLHttpRequest();
          xhr.open('POST', url, true);
          xhr.setRequestHeader('Content-Type', 'application/json');

          xhr.onload = function() {
            if (xhr.status === 200) {
              try {
                const result = JSON.parse(xhr.responseText);
                resolve(result);
              } catch (e) {
                reject(new Error('API Response Parsing Error.'));
              }
            } else {
              if (xhr.status === 400) {
                reject(new Error('Invalid Request: प्रॉम्प्ट या इनपुट में त्रुटि। कृपया जांचें।'));
              } else if (xhr.status === 403) {
                reject(new Error('API Key Error: API Key गलत है या कोटा खत्म हो गया है। Google Cloud Console में जांचें।'));
              } else if (xhr.status === 429) {
                reject(new Error('Quota Exceeded: बहुत सारी रिक्वेस्ट। कृपया बाद में पुनः प्रयास करें।'));
              } else {
                reject(new Error(`Server Error: HTTP ${xhr.status}`));
              }
            }
          };

          xhr.onerror = function() {
            reject(new Error('Network Error: कृपया अपना इंटरनेट कनेक्शन जांचें।'));
          };

          xhr.timeout = 60000;
          xhr.send(JSON.stringify(payload));
        });
      }

      // YouTube API Fetch
      async function callYouTubeAPI(endpoint, params) {
        try {
          const response = await gapi.client.youtube[endpoint].list(params);
          return response.result;
        } catch (error) {
          if (error.status === 403) {
            throw new Error('YouTube API Quota Exceeded or Invalid Key: Google Cloud Console में API Key या Quota जांचें।');
          } else if (error.status === 400) {
            throw new Error('Invalid Input: कृपया सही लिंक या Niche डालें।');
          } else {
            throw new Error(`YouTube API Error: ${error.result?.error?.message || error.message}`);
          }
        }
      }

      // Update UI
      function updateOutput(outputId, content, type = 'text') {
        const outputDiv = document.getElementById(outputId);
        if (!outputDiv) return;

        if (type === 'error') {
          outputDiv.innerHTML = `
            <div class="text-red-500 font-bold mb-2 flex items-center space-x-2">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.3 16c-.77 1.333.192 3 1.732 3z"/></svg>
              <span>त्रुटि (Error)</span>
            </div>
            <p class="text-gray-300">${content}</p>
            <p class="text-yellow-400 mt-2">समस्या जारी रहने पर अपनी API Key जांचें या support@youtubevistarsalahkar.com से संपर्क करें।</p>
          `;
        } else if (type === 'image') {
          outputDiv.innerHTML = `<img src="${content}" alt="Generated Thumbnail" class="max-w-full h-auto rounded-lg shadow-xl border-4 border-yt-red/50">`;
        } else {
          outputDiv.textContent = content;
        }
      }

      // Toggle Loading
      function toggleLoading(loaderId, button, isLoading) {
        const loader = document.getElementById(loaderId);
        const submitText = button.querySelector('.submit-text');
        if (isLoading) {
          button.classList.add('loading');
          loader.style.display = 'block';
          submitText.style.display = 'none';
          button.disabled = true;
        } else {
          button.classList.remove('loading');
          loader.style.display = 'none';
          submitText.style.display = 'block';
          button.disabled = false;
        }
      }

      // Update UI Language
      function updateUILanguage(lang) {
        document.querySelector('#video-seo button .submit-text').textContent = translations[lang].seoButton;
        document.getElementById('seo-topic').placeholder = translations[lang].seoPlaceholder;
        document.querySelector('#channel-audit button .submit-text').textContent = translations[lang].auditButton;
        document.getElementById('audit-link').placeholder = translations[lang].auditPlaceholder;
        document.querySelector('#trending-ideas button .submit-text').textContent = translations[lang].trendButton;
        document.getElementById('trend-niche').placeholder = translations[lang].trendPlaceholder;
        document.querySelector('#script-story button .submit-text').textContent = translations[lang].scriptButton;
        document.getElementById('script-topic').placeholder = translations[lang].scriptPlaceholder;
        document.querySelector('#thumbnail-maker button .submit-text').textContent = translations[lang].thumbnailButton;
        document.getElementById('thumbnail-prompt').placeholder = translations[lang].thumbnailPlaceholder;
      }

      // Tab Switching
      document.querySelectorAll('.tab-button').forEach(button => {
        button.addEventListener('click', () => {
          document.querySelectorAll('.tab-button').forEach(btn => btn.classList.remove('active', 'text-yt-red', 'font-bold'));
          document.querySelectorAll('.tab-pane').forEach(pane => pane.classList.add('hidden'));

          button.classList.add('active', 'text-yt-red', 'font-bold');
          document.getElementById(button.dataset.tab).classList.remove('hidden');
        });
      });

      // Gemini API Call
      async function callGemini(systemPrompt, userQuery) {
        const selectedLanguage = document.getElementById('language-select').value;
        const payload = {
          contents: [{ parts: [{ text: userQuery }] }],
          tools: [{ "google_search": {} }],
          systemInstruction: {
            parts: [{ text: `${systemPrompt}। आपका आउटपुट पूरी तरह से ${selectedLanguage} भाषा में होना चाहिए।` }]
          },
        };
        const url = `https://generativelanguage.googleapis.com/v1beta/models/${GEMINI_MODEL}:generateContent?key=${GEMINI_API_KEY}`;
        const result = await callAPI(url, payload);
        return result?.candidates?.[0]?.content?.parts?.[0]?.text || "AI परिणाम प्राप्त नहीं हुआ।";
      }

      // Imagen API Call
      async function callImagen(prompt) {
        const payload = {
          contents: [{ parts: [{ text: prompt }] }],
          generationConfig: { response_mime_type: 'image/png' }
        };
        const url = `https://generativelanguage.googleapis.com/v1beta/models/${IMAGEN_MODEL}:generateContent?key=${GEMINI_API_KEY}`;
        const result = await callAPI(url, payload);
        return result?.candidates?.[0]?.content?.parts?.[0]?.inlineData?.data;
      }

      // Feature Handlers
      async function handleVideoOptimization(outputId, topicId) {
        const topic = document.getElementById(topicId).value.trim();
        const loaderId = 'seo-loader';
        const button = document.querySelector(`#video-seo button`);

        if (!topic || topic.length < 3) return updateOutput(outputId, 'कृपया कम से कम 3 अक्षरों का विषय दर्ज करें।', 'error');

        try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'AI द्वारा SEO सामग्री जनरेट की जा रही है... कृपया प्रतीक्षा करें।');
          
          const systemPrompt = "आप एक विशेषज्ञ YouTube SEO सलाहकार हैं। दिए गए विषय के लिए, 1. दो शीर्षक (एक SEO-अनुकूल, एक क्लिक-आकर्षक, 60-70 अक्षर), 2. एक विस्तृत विवरण (150-200 शब्द, हैशटैग, CTA, टाइमस्टैम्प placeholder), और 3. 10 सबसे प्रभावी टैग प्रदान करें। आउटपुट स्पष्ट और संरचित हो।";
          const userQuery = `विषय: ${topic}`;

          const rawText = await callGemini(systemPrompt, userQuery);
          updateOutput(outputId, rawText, 'text');
        } catch (e) {
          updateOutput(outputId, `SEO जनरेशन विफल: ${e.message}`, 'error');
        } finally {
          toggleLoading(loaderId, button, false);
        }
      }

      async function handleChannelAudit(outputId, linkId) {
        const link = document.getElementById(linkId).value.trim();
        const loaderId = 'audit-loader';
        const button = document.querySelector(`#channel-audit button`);

        if (!link || !link.includes('youtube.com')) return updateOutput(outputId, 'कृपया वैध YouTube चैनल लिंक दर्ज करें।', 'error');

        try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'YouTube API द्वारा चैनल का विश्लेषण किया जा रहा है... कृपया प्रतीक्षा करें।');

          const channelIdMatch = link.match(/(?:youtube\.com\/(?:@|c\/|channel\/|user\/)?)([^\/]+)/);
          const channelId = channelIdMatch ? channelIdMatch[1] : link;

          const channelData = await callYouTubeAPI('channels', {
            part: 'snippet,statistics,brandingSettings',
            forHandle: channelId.startsWith('@') ? channelId : null,
            id: !channelId.startsWith('@') ? channelId : null
          });

          if (!channelData.items || channelData.items.length === 0) {
            throw new Error('चैनल नहीं मिला। कृपया सही लिंक या ID डालें।');
          }

          const channel = channelData.items[0];
          const stats = channel.statistics;
          const snippet = channel.snippet;

          const systemPrompt = "आप एक YouTube ग्रोथ विशेषज्ञ हैं। दिए गए चैनल की जानकारी के आधार पर, 1. मुख्य कमियाँ (What is Missing), 2. ग्रोथ के लिए 5 ठोस कदम (What to Do) प्रदान करें। आउटपुट संक्षिप्त और स्पष्ट हो।";
          const userQuery = `चैनल: ${snippet.title}, सब्सक्राइबर्स: ${stats.subscriberCount}, कुल व्यूज: ${stats.viewCount}, वीडियो की संख्या: ${stats.videoCount}, विवरण: ${snippet.description}`;

          const suggestions = await callGemini(systemPrompt, userQuery);
          
          const output = `
चैनल: ${snippet.title}
सब्सक्राइबर्स: ${stats.subscriberCount || 'निजी'}
कुल व्यूज: ${stats.viewCount || 'निजी'}
वीडियो की संख्या: ${stats.videoCount || 'निजी'}
विवरण: ${snippet.description || 'कोई विवरण नहीं'}

AI सुझाव:
${suggestions}
          `;
          updateOutput(outputId, output, 'text');
        } catch (e) {
          updateOutput(outputId, `ऑडिट जनरेशन विफल: ${e.message}`, 'error');
        } finally {
          toggleLoading(loaderId, button, false);
        }
      }

      async function handleTrendGeneration(outputId, nicheId) {
        const niche = document.getElementById(nicheId).value.trim();
        const loaderId = 'trend-loader';
        const button = document.querySelector(`#trending-ideas button`);

        if (!niche || niche.length < 3) return updateOutput(outputId, 'कृपया कम से कम 3 अक्षरों की Niche दर्ज करें।', 'error');

        try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'YouTube API द्वारा ट्रेंडिंग विचार खोजे जा रहे हैं... कृपया प्रतीक्षा करें।');

          const videos = await callYouTubeAPI('search', {
            part: 'snippet',
            q: niche,
            type: 'video',
            order: 'viewCount',
            regionCode: 'IN',
            maxResults: 5
          });

          if (!videos.items || videos.items.length === 0) {
            throw new Error('कोई ट्रेंडिंग वीडियो नहीं मिला। कृपया दूसरी Niche आजमाएँ।');
          }

          const systemPrompt = "आप एक मार्केट रिसर्च एक्सपर्ट हैं। दिए गए Niche और YouTube ट्रेंडिंग वीडियो डेटा के आधार पर, 5 क्लिक-योग्य और ट्रेंडिंग वीडियो टॉपिक्स दें। प्रत्येक टॉपिक में शीर्षक और संक्षिप्त विवरण हो।";
          const videoList = videos.items.map(item => `${item.snippet.title} (https://youtube.com/watch?v=${item.id.videoId})`).join('\n');
          const userQuery = `Niche: ${niche}\nट्रेंडिंग वीडियो: ${videoList}`;

          const suggestions = await callGemini(systemPrompt, userQuery);
          
          const output = `
ट्रेंडिंग विचार (${niche}):
${suggestions}
          `;
          updateOutput(outputId, output, 'text');
        } catch (e) {
          updateOutput(outputId, `ट्रेंड जनरेशन विफल: ${e.message}`, 'error');
        } finally {
          toggleLoading(loaderId, button, false);
        }
      }

      async function handleScriptGeneration(outputId, topicId, styleId) {
        const topic = document.getElementById(topicId).value.trim();
        const style = document.getElementById(styleId).value;
        const loaderId = 'script-loader';
        const button = document.querySelector(`#script-story button`);

        if (!topic || topic.length < 3) return updateOutput(outputId, 'कृपया कम से कम 3 अक्षरों का विषय दर्ज करें।', 'error');

        try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, `AI द्वारा ${style} स्टाइल में स्क्रिप्ट लिखी जा रही है... कृपया प्रतीक्षा करें।`);

          const systemPrompt = `आप एक पेशेवर पटकथा लेखक हैं। दिए गए विषय और स्टाइल के आधार पर, एक विस्तृत (कम से कम 300 शब्द), बोलने योग्य वीडियो स्क्रिप्ट (हुक, 3 मुख्य बिंदु, निष्कर्ष/CTA सहित) और एक भावनात्मक रूप से आकर्षक स्टोरी आइडिया (Emotional Hook) तैयार करें।`;
          const userQuery = `विषय: ${topic}, स्टाइल: ${style}`;

          const rawText = await callGemini(systemPrompt, userQuery);
          updateOutput(outputId, rawText, 'text');
        } catch (e) {
          updateOutput(outputId, `स्क्रिप्ट जनरेशन विफल: ${e.message}`, 'error');
        } finally {
          toggleLoading(loaderId, button, false);
        }
      }

      async function handleThumbnailGeneration(outputId, promptId) {
        const prompt = document.getElementById(promptId).value.trim();
        const loaderId = 'thumbnail-loader';
        const button = document.querySelector(`#thumbnail-maker button`);

        if (!prompt || prompt.length < 10) return updateOutput(outputId, 'कृपया कम से कम 10 अक्षरों का थंबनेल विवरण दर्ज करें।', 'error');

        try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'AI द्वारा थंबनेल बनाया जा रहा है... कृपया प्रतीक्षा करें।');

          const rawBase64 = await callImagen(prompt);
          
          if (rawBase64) {
            const imageUrl = `data:image/png;base64,${rawBase64}`;
            updateOutput(outputId, imageUrl, 'image');
          } else {
            updateOutput(outputId, 'थंबनेल बनाने में असमर्थ। कृपया प्रॉम्प्ट बदलें या API Key जांचें।', 'error');
          }
        } catch (e) {
          updateOutput(outputId, `थंबनेल जनरेशन विफल: ${e.message}`, 'error');
        } finally {
          toggleLoading(loaderId, button, false);
        }
      }

      // Initialize
      document.addEventListener('DOMContentLoaded', () => {
        setUserIdDisplay();
        initYouTubeAPI();
        document.querySelector('.tab-button').click();
        document.getElementById('language-select').addEventListener('change', e => updateUILanguage(e.target.value));
        updateUILanguage('Hindi'); // Default
      });
    </script>
</body>
</html>
