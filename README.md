
<meta name="google-site-verification" content="IBIxq7l1jTl5OYSP1t3NebJUiZ9_neYoZncfr7xwWxE" />
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          'yt-red': '#FF0000',
          'yt-dark': '#0f0f0f',
          'yt-light': '#ffffff',
          'yt-grey': '#272727',
          'yt-med-grey': '#333333',
        },
        fontFamily: {
          sans: ['Inter', 'sans-serif'],
        },
      }
    }
  }
</script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800;900&display=swap');
  
  body {
    background-color: #0f0f0f;
    color: #ffffff;
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
  }
  
  .tab-button.active {
    border-bottom: 3px solid #FF0000;
    color: #FF0000;
    font-weight: 700;
    background-color: #1a1a1a;
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
  
  .loading .loader {
    display: block;
  }
  .loading .submit-text {
    display: none;
  }

  @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }

  /* Custom input styling */
  input[type="text"], textarea, select {
    background-color: #1a1a1a !important;
    border: 1px solid #333333 !important;
    color: #ffffff !important;
    border-radius: 8px !important;
    padding: 10px !important;
  }
  
  /* Styling for the User ID box */
  .user-id-box {
    background-color: #272727;
    border: 1px dashed #FF0000;
    padding: 8px 12px;
    border-radius: 8px;
    font-size: 0.8rem;
    color: #FFDDDD;
  }
</style>

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
         <select id="language-select" class="bg-yt-dark text-yt-light rounded-md p-2 border border-yt-grey text-sm focus:ring-yt-red focus:border-yt-red">
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

  <main class="flex-grow max-w-7xl mx-auto w-full px-4 sm:px-6 lg:px-8 py-6">
    <div class="flex border-b border-yt-grey overflow-x-auto whitespace-nowrap mb-6">
      <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300 active" data-tab="video-seo">🎬 वीडियो SEO</button>
      <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="channel-audit">📈 चैनल समीक्षा</button>
      <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="trending-ideas">🔥 ट्रेंडिंग विचार</button>
      <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="script-story">✍️ स्क्रिप्ट / स्टोरी</button>
      <button class="tab-button px-4 py-3 text-center text-sm font-medium transition duration-300" data-tab="thumbnail-maker">🖼️ थंबनेल मेकर</button>
    </div>
    
    <div class="w-full mb-6 mt-4">
        <div class="bg-yt-med-grey p-3 rounded-xl border border-yt-grey text-center shadow-lg">
            <p class="text-xs font-semibold text-gray-400 mb-2 uppercase tracking-wider">Advertisement / प्रायोजक</p>
            
            <div id="top-banner-ad" class="w-full bg-yt-dark py-4 rounded-lg flex items-center justify-center min-h-[90px]">
                <p class="text-gray-500 font-medium text-sm">
                    [ Google AdSense Code Ya Custom Image Banner Yahan Aayega ]
                </p>
            </div>
            </div>
    </div>
    <div id="tab-content">
      <div id="video-seo" class="tab-pane active space-y-6">
        <h2 class="text-2xl font-bold text-yt-red">🎬 वीडियो SEO</h2>
        <input type="text" id="seo-topic" placeholder="आपके वीडियो का मुख्य विषय क्या है? (जैसे: ब्लॉग्गिंग से पैसे कैसे कमाएं)" class="w-full">
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
        <input type="text" id="audit-link" placeholder="अपने YouTube चैनल या वीडियो का लिंक पेस्ट करें (उदा: https://youtube.com/@TechChannel)" class="w-full">
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
        <input type="text" id="trend-niche" placeholder="अपने चैनल की श्रेणी या Niche डालें (उदा: टेक्नोलॉजी, कुकिंग, फाइनेंस)" class="w-full">
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
        <input type="text" id="script-topic" placeholder="आपके वीडियो का विषय (उदा: इतिहास का सबसे बड़ा रहस्य)" class="w-full">
        <select id="script-style" class="w-full bg-yt-dark text-yt-light rounded-md p-3 border border-yt-grey focus:ring-yt-red focus:border-yt-red">
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
        <textarea id="thumbnail-prompt" rows="3" placeholder="थंबनेल का विस्तृत विवरण दें (उदा: एक हैरान आदमी ₹1 लाख के नोट पकड़े हुए, टेक्स्ट 'HOW I EARNED IT' बड़े अक्षरों में)" class="w-full"></textarea>
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
    <p>Powered by Gemini AI and Imagen 3.0. Designed for YouTube Creators.</p>
  </footer>
</div>

<script>
  // --- Global Setup and Utility Functions ---
  const GEMINI_MODEL = "gemini-2.5-flash-preview-05-20";
  const IMAGEN_MODEL = "imagen-3.0-generate-002";
  
  // ****** YAHAN AAPKI GEMINI API KEY PASTE KI GAYI HAI ******
  // Note: Your key should be exactly inside the quotes, without extra spaces or quotes.
  const apiKey = "AIzaSyDdvSRrEzB8YbQ8F_8PyYKmPUfPA_GQ_xU"; 
  // ****************************************************

  let userId = 'USER-' + (crypto.randomUUID ? crypto.randomUUID() : Math.random().toString(36).substring(2, 9));

  function setUserIdDisplay() {
      document.getElementById('user-id').textContent = userId;
  }
  
  // XHR Utility for making AI calls (used for better stability)
  function callAPI(url, payload, isImage = false) {
    return new Promise((resolve, reject) => {
      // API Key Check
      if (apiKey === "YOUR_GEMINI_API_KEY_HERE" || !apiKey) {
           return reject(new Error('API Key Missing: कृपया कोड में अपनी API Key डालें।'));
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
            console.error("API Response Parsing Error:", e);
            reject(new Error('API Response Parsing Error.'));
          }
        } else {
          console.error(`API Call Failed with status: ${xhr.status}, response: ${xhr.responseText}`);
          // Provide more helpful error for unauthorized/quota issues
          if (xhr.status === 400 || xhr.status === 403) {
             reject(new Error(`API त्रुटि (HTTP ${xhr.status}): आपकी API Key गलत हो सकती है या आपका कोटा खत्म हो गया है।`));
          } else {
             reject(new Error(`सर्वर त्रुटि: HTTP ${xhr.status}`));
          }
        }
      };

      xhr.onerror = function() {
        console.error("Network Error during API Call.");
        reject(new Error('नेटवर्क त्रुटि: सर्वर तक नहीं पहुँचा जा सका।'));
      };
      
      xhr.timeout = 60000; // 60 seconds timeout
      xhr.send(JSON.stringify(payload));
    });
  }

  // Helper to update UI (Error or Success)
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
        <p class="text-yellow-400 mt-2">समस्या जारी रहने पर अपनी API Key जांचें।</p>
      `;
    } else if (type === 'image') {
        outputDiv.innerHTML = `<img src="${content}" alt="Generated Thumbnail" class="max-w-full h-auto rounded-lg shadow-xl border-4 border-yt-red/50">`;
    } else {
      outputDiv.textContent = content;
    }
  }
  
  // Helper to toggle loading state
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


  // --- Tab Switching Logic ---
  document.querySelectorAll('.tab-button').forEach(button => {
    button.addEventListener('click', () => {
      document.querySelectorAll('.tab-button').forEach(btn => btn.classList.remove('active', 'text-yt-red', 'font-bold'));
      document.querySelectorAll('.tab-pane').forEach(pane => pane.classList.add('hidden'));

      button.classList.add('active', 'text-yt-red', 'font-bold');
      document.getElementById(button.dataset.tab).classList.remove('hidden');
    });
  });

  // --- Core API Functions ---

  async function callGemini(systemPrompt, userQuery) {
    const selectedLanguage = document.getElementById('language-select').value;

    const payload = {
        contents: [{ parts: [{ text: userQuery }] }],
        tools: [{ "google_search": {} }],
        systemInstruction: {
            parts: [{ text: `${systemPrompt}। आपका आउटपुट पूरी तरह से ${selectedLanguage} भाषा में होना चाहिए।` }]
        },
    };

    const url = `https://generativelanguage.googleapis.com/v1beta/models/${GEMINI_MODEL}:generateContent?key=${apiKey}`;

    const result = await callAPI(url, payload);
    return result?.candidates?.[0]?.content?.parts?.[0]?.text || "AI परिणाम प्राप्त नहीं हुआ।";
  }

  async function callImagen(prompt) {
    const payload = {
        instances: [{ prompt: prompt }],
        parameters: { "sampleCount": 1 }
    };
    
    const url = `https://generativelanguage.googleapis.com/v1beta/models/${IMAGEN_MODEL}:predict?key=${apiKey}`;

    const result = await callAPI(url, payload);
    return result?.predictions?.[0]?.bytesBase64Encoded;
  }
  

  // --- Feature Handlers ---

  async function handleVideoOptimization(outputId, topicId) {
      const topic = document.getElementById(topicId).value.trim();
      const loaderId = 'seo-loader';
      const button = document.querySelector(`#video-seo button`);

      if (!topic) return updateOutput(outputId, 'कृपया वीडियो का विषय दर्ज करें।', 'error');

      try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'AI द्वारा SEO सामग्री जनरेट की जा रही है... कृपया प्रतीक्षा करें।');
          
          const systemPrompt = "आप एक विशेषज्ञ YouTube SEO सलाहकार हैं। दिए गए विषय के लिए, 1. दो शीर्षक (एक SEO-अनुकूल, एक क्लिक-आकर्षक), 2. एक विस्तृत विवरण (जिसमें हैशटैग, CTA, और टाइमस्टैम्प का Placeholder हो), और 3. 10 सबसे प्रभावी टैग प्रदान करें। आउटपुट को स्पष्ट रूप से फॉर्मेट करें।";
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

      if (!link) return updateOutput(outputId, 'कृपया चैनल या वीडियो का लिंक दर्ज करें।', 'error');

      try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'AI द्वारा चैनल का विश्लेषण किया जा रहा है... कृपया प्रतीक्षा करें।');

          const systemPrompt = "आप एक YouTube ग्रोथ विशेषज्ञ हैं। दिए गए चैनल/वीडियो लिंक का विश्लेषण करें (सार्वजनिक जानकारी के आधार पर)। 1. मुख्य कमियाँ (What is Missing), 2. ग्रोथ के लिए 5 ठोस कदम (What to Do) प्रदान करें।";
          const userQuery = `चैनल/वीडियो लिंक: ${link}`;

          const rawText = await callGemini(systemPrompt, userQuery);
          
          updateOutput(outputId, rawText, 'text');

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

      if (!niche) return updateOutput(outputId, 'कृपया अपने चैनल की Niche (श्रेणी) दर्ज करें।', 'error');

      try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'AI द्वारा ट्रेंडिंग विचारों की खोज की जा रही है... कृपया प्रतीक्षा करें।');

          const systemPrompt = "आप एक मार्केट रिसर्च एक्सपर्ट हैं। दिए गए Niche से संबंधित, Google Search Grounding का उपयोग करके 5 सबसे वर्तमान (Trending) और क्लिक-योग्य वीडियो टॉपिक के आइडिया दें। हर टॉपिक को स्पष्ट शीर्षक और संक्षिप्त विवरण के साथ प्रदान करें।";
          const userQuery = `Niche: ${niche}`;

          const rawText = await callGemini(systemPrompt, userQuery);
          
          updateOutput(outputId, rawText, 'text');

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

      if (!topic) return updateOutput(outputId, 'कृपया स्क्रिप्ट के लिए विषय दर्ज करें।', 'error');

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

      if (!prompt) return updateOutput(outputId, 'कृपया थंबनेल का विस्तृत विवरण दर्ज करें।', 'error');

      try {
          toggleLoading(loaderId, button, true);
          updateOutput(outputId, 'AI द्वारा थंबनेल बनाया जा रहा है... कृपया प्रतीक्षा करें।');

          const rawBase64 = await callImagen(prompt);
          
          if (rawBase64) {
              const imageUrl = `data:image/jpeg;base64,${rawBase64}`;
              updateOutput(outputId, imageUrl, 'image');
          } else {
              updateOutput(outputId, 'थंबनेल बनाने में असमर्थ। कृपया प्रॉम्प्ट बदलें।', 'error');
          }

      } catch (e) {
          updateOutput(outputId, `थंबनेल जनरेशन विफल: ${e.message}`, 'error');
      } finally {
          toggleLoading(loaderId, button, false);
      }
  }
  
  // Initialize on load
  document.addEventListener('DOMContentLoaded', () => {
    setUserIdDisplay();
    
    // Auto-select the first tab
    document.querySelector('.tab-button').click();
  });
</script>
