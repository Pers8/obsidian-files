TThe console :

Uncaught ReferenceError: path is not defined

at D (main-MntAaLrb.js:113:52315)

at onChange (main-MntAaLrb.js:117:972)

at Ay (main-MntAaLrb.js:48:116423)

at main-MntAaLrb.js:48:121413

at Dg (main-MntAaLrb.js:48:9041)

at Fs (main-MntAaLrb.js:48:117650)

at tf (main-MntAaLrb.js:49:26598)

at SS (main-MntAaLrb.js:49:26420)

I have 8 tabs right, before I close a tab, it looks like this (the html file) :

<html lang="en"><head><style data-merge-styles="true"></style>

<meta charset="UTF-8">

<link rel="icon" type="image/png" href="/icon.png">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Spritesheet Generator</title>

<script type="module" crossorigin="" src="./assets/main-MntAaLrb.js"></script>

<link rel="stylesheet" crossorigin="" href="./assets/main-CRz7WBsT.css">

</head>

<body>

<div id="root"><div class="bg-[#18191C] text-white min-h-screen font-sans px-6 py-8"><h1 class="text-2xl font-semibold text-center mb-6">Spritesheet Generator</h1><div class="flex items-center mb-5 space-x-2 overflow-x-auto"><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 1</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 2</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 3</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 4</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 5</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 6</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

hover:bg-white/5

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 7</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><div draggable="true" class="

px-4 py-2 rounded-xl flex items-center gap-2 text-sm

border border-white/10

bg-white/10

"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-grip-vertical cursor-move opacity-50" aria-hidden="true"><circle cx="9" cy="12" r="1"></circle><circle cx="9" cy="5" r="1"></circle><circle cx="9" cy="19" r="1"></circle><circle cx="15" cy="12" r="1"></circle><circle cx="15" cy="5" r="1"></circle><circle cx="15" cy="19" r="1"></circle></svg><span>Session 8</span><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-pen cursor-pointer" aria-hidden="true"><path d="M12 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.375 2.625a1 1 0 0 1 3 3l-9.013 9.014a2 2 0 0 1-.853.505l-2.873.84a.5.5 0 0 1-.62-.62l.84-2.873a2 2 0 0 1 .506-.852z"></path></svg><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-trash2 lucide-trash-2 cursor-pointer text-red-400" aria-hidden="true"><path d="M3 6h18"></path><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"></path><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"></path><line x1="10" x2="10" y1="11" y2="17"></line><line x1="14" x2="14" y1="11" y2="17"></line></svg></div><button class="p-2 rounded-lg bg-white/10 hover:bg-white/20"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-plus" aria-hidden="true"><path d="M5 12h14"></path><path d="M12 5v14"></path></svg></button></div><input multiple="" accept="image/*" class="hidden" type="file"><div class="

w-full h-48 rounded-lg border-2 border-dashed flex items-center justify-center

cursor-pointer mb-4 relative transition-colors

border-white/10

"><svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-folder-plus opacity-80 mb-2" aria-hidden="true"><path d="M12 10v6"></path><path d="M9 13h6"></path><path d="M20 20a2 2 0 0 0 2-2V8a2 2 0 0 0-2-2h-7.9a2 2 0 0 1-1.69-.9L9.6 3.9A2 2 0 0 0 7.93 3H4a2 2 0 0 0-2 2v13a2 2 0 0 0 2 2Z"></path></svg><p class="text-sm">Drag &amp; drop or click to browse</p></div><div class="mb-4"><label class="text-sm block mb-1">Output Folder</label><button class="w-full bg-white/5 text-left px-4 py-2 rounded-lg flex items-center justify-between hover:bg-white/10"><span class="truncate">C:\Users\peres\OneDrive\Images\TurnerMainMenu\Assets\SpriteSheets\ScrollCloud</span><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-folder-plus opacity-70" aria-hidden="true"><path d="M12 10v6"></path><path d="M9 13h6"></path><path d="M20 20a2 2 0 0 0 2-2V8a2 2 0 0 0-2-2h-7.9a2 2 0 0 1-1.69-.9L9.6 3.9A2 2 0 0 0 7.93 3H4a2 2 0 0 0-2 2v13a2 2 0 0 0 2 2Z"></path></svg></button></div><div class="flex items-center gap-4 mb-4"><label class="text-sm">Export as:</label><select class="bg-white/5 px-3 py-1 rounded-lg text-sm"><option value="png">PNG</option><option value="gif">GIF</option></select></div></div></div>

<!-- Add this to load your app -->

</body></html>

And when I click to delete a tab, it looks like this :

<html lang="en"><head><style data-merge-styles="true"></style>

<meta charset="UTF-8">

<link rel="icon" type="image/png" href="/icon.png">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Spritesheet Generator</title>

<script type="module" crossorigin="" src="./assets/main-MntAaLrb.js"></script>

<link rel="stylesheet" crossorigin="" href="./assets/main-CRz7WBsT.css">

</head>

<body>

<div id="root"></div>

<!-- Add this to load your app -->

</body></html>

Also Idk why I can't upload files bc when I try to, it basically does nothing basically. You messed up a lot of previous feature




































import { useState, useEffect, useRef } from "react"; import { motion, AnimatePresence } from "framer-motion"; import { Bell, FolderPlus, Plus, Trash2, Edit, Undo2, GripVertical } from "lucide-react"; import { initializeIcons } from '@fluentui/react'; initializeIcons(); const STAGES = ["Uploading", "Processing Files", "Creating Spritesheet", "Finishing Up"]; export default function SpritesheetGenerator() { const [tabs, setTabs] = useState(() => { const saved = localStorage.getItem("spritesheet-tabs"); return saved ? JSON.parse(saved) : [{ id: 1, name: "Session 1", data: { history: [] } }]; }); const [activeTabId, setActiveTabId] = useState(() => { const saved = localStorage.getItem("spritesheet-active-tab"); return saved ? JSON.parse(saved) : 1; }); const [undoStack, setUndoStack] = useState([]); const [renamingId, setRenamingId] = useState(null); const [newName, setNewName] = useState(""); const [progress, setProgress] = useState(0); const [notification, setNotification] = useState(null); const [progressStage, setProgressStage] = useState(0); const dragTabId = useRef(null); const activeTab = tabs.find((t) => t.id === activeTabId); const setActiveTabData = (data) => { setTabs((prev) => prev.map((t) => t.id === activeTabId ? { ...t, data: { ...t.data, ...data } } : t)); }; useEffect(() => { localStorage.setItem("spritesheet-tabs", JSON.stringify(tabs)); localStorage.setItem("spritesheet-active-tab", JSON.stringify(activeTabId)); }, [tabs, activeTabId]); const handleDrop = (e) => { e.preventDefault(); const files = Array.from(e.dataTransfer.files).slice(0, 100); const fileURLs = files.map(f => URL.createObjectURL(f)); const dimensions = files.map(f => ({ name: f.name, size: `${Math.round(f.size / 1024)} KB` })); setActiveTabData({ folderPath: files[0]?.webkitRelativePath?.split("/")[0], previews: fileURLs, grid: dimensions, canGenerate: true }); }; const generateSpritesheet = () => { const { folderPath, outputFolderPath, exportType, history = [] } = activeTab?.data || {}; if (!folderPath || !outputFolderPath) return; setProgress(0); setProgressStage(0); setNotification(null); setActiveTabData({ canGenerate: false }); let prog = 0; const interval = setInterval(() => { prog += 5; setProgress(prog); setProgressStage(Math.floor(prog / 25)); if (prog >= 100) { clearInterval(interval); const timestamp = new Date().toLocaleTimeString(); setNotification(`Spritesheet (${exportType?.toUpperCase() || "PNG"}) generated successfully.`); setActiveTabData({ history: [...history, { type: exportType, time: timestamp }] }); setTimeout(() => setProgress(0), 1500); } }, 150); }; const handleTabDragStart = (id) => { dragTabId.current = id; }; const handleTabDrop = (id) => { if (dragTabId.current === null) return; const draggedIndex = tabs.findIndex((t) => t.id === dragTabId.current); const droppedIndex = tabs.findIndex((t) => t.id === id); const newTabs = [...tabs]; const [dragged] = newTabs.splice(draggedIndex, 1); newTabs.splice(droppedIndex, 0, dragged); setTabs(newTabs); dragTabId.current = null; }; return ( <div className="bg-[#18191C] text-white min-h-screen font-sans px-4 py-6"> <h1 className="text-2xl font-semibold text-center mb-6">Spritesheet Generator</h1> <div className="flex items-center mb-4 space-x-2 overflow-x-auto"> {tabs.map((tab) => ( <motion.div key={tab.id} draggable onDragStart={() => handleTabDragStart(tab.id)} onDragOver={(e) => e.preventDefault()} onDrop={() => handleTabDrop(tab.id)} className={`px-4 py-2 rounded-xl flex items-center gap-2 text-sm border border-white/10 ${tab.id === activeTabId ? "bg-white/10" : "hover:bg-white/5"}`} onClick={() => setActiveTabId(tab.id)} > <GripVertical size={12} className="cursor-move opacity-50" /> {renamingId === tab.id ? ( <input autoFocus value={newName} onChange={(e) => setNewName(e.target.value)} onBlur={() => { setTabs(tabs.map(t => t.id === tab.id ? { ...t, name: newName } : t)); setRenamingId(null); }} onKeyDown={(e) => e.key === "Enter" && setTabs(tabs.map(t => t.id === tab.id ? { ...t, name: newName } : t))} className="bg-transparent border-none outline-none text-white text-sm" /> ) : <span>{tab.name}</span>} <Edit size={14} onClick={() => { setRenamingId(tab.id); setNewName(tab.name); }} className="cursor-pointer hover:text-gray-300" /> {tabs.length > 1 && <Trash2 size={14} onClick={() => { setUndoStack([...undoStack, tab]); setTabs(tabs.filter(t => t.id !== tab.id)); if (tab.id === activeTabId) setActiveTabId(tabs[0].id); }} className="cursor-pointer text-red-400 hover:text-red-600" />} </motion.div> ))} <button onClick={() => tabs.length < 10 && setTabs([...tabs, { id: Date.now(), name: `Session ${tabs.length + 1}`, data: {} }])} className="p-2 rounded-lg bg-white/10 hover:bg-white/20"> <Plus size={16} /> </button> {undoStack.length > 0 && <button onClick={() => { const restored = undoStack.pop(); setTabs([...tabs, restored]); setActiveTabId(restored.id); setUndoStack([...undoStack]); }} className="p-2 rounded-lg bg-white/10 hover:bg-white/20" title="Undo delete"> <Undo2 size={16} /> </button>} </div> <div onDragOver={(e) => { e.preventDefault(); }} onDrop={handleDrop} className="w-full h-48 rounded-lg border-2 border-dashed border-white/10 flex flex-col items-center justify-center text-sm"> <FolderPlus size={40} className="mb-2 opacity-80" /> Drag & drop files or <span className="underline cursor-pointer">browse</span> </div> {activeTab?.data?.folderPath && <p className="mt-2 text-sm text-gray-400">Input: {activeTab.data.folderPath}</p>} <div className="mt-4"> <label className="text-sm block mb-1">Output Folder</label> <div className="bg-white/5 rounded-lg overflow-hidden relative"> <input type="file" webkitdirectory="true" onChange={(e) => setActiveTabData({ outputFolderPath: e.target.files[0]?.webkitRelativePath?.split("/")[0] })} className="w-full opacity-0 absolute top-0 left-0 h-full cursor-pointer" /> <div className="px-4 py-2 text-sm">{activeTab?.data?.outputFolderPath || "Click to choose folder..."}</div> </div> </div> <div className="mt-4 flex gap-4 items-center"> <label className="text-sm">Export as:</label> <select value={activeTab?.data?.exportType || "png"} onChange={(e) => setActiveTabData({ exportType: e.target.value })} className="bg-white/5 text-white px-4 py-2 rounded-lg text-sm"> <option value="png">PNG</option> <option value="gif">GIF</option> </select> </div> {activeTab?.data?.canGenerate && activeTab?.data?.outputFolderPath && ( <motion.button initial={{ opacity: 0 }} animate={{ opacity: 1 }} whileHover={{ scale: 1.05 }} onClick={generateSpritesheet} className="mt-4 px-6 py-2 bg-[#7289DA] text-white rounded-lg"> Generate Spritesheet </motion.button> )} {activeTab?.data?.previews?.length > 0 && ( <div className="relative mt-6 max-h-48 overflow-y-auto scrollbar-thin scrollbar-thumb-white/20 scrollbar-track-transparent pr-2 rounded-xl"> <div className="grid grid-cols-6 gap-2"> {activeTab.data.previews.map((src, i) => ( <div key={i} className="bg-white/5 rounded-lg overflow-hidden"> <img src={src} alt={`Frame ${i}`} className="w-full h-16 object-cover" /> </div> ))} </div> <div className="absolute bottom-0 left-0 right-0 h-8 bg-gradient-to-t from-[#18191C] to-transparent pointer-events-none rounded-b-xl" /> </div> )} {activeTab?.data?.grid?.length > 0 && ( <div className="mt-2 text-xs text-gray-400"> {activeTab.data.grid.length} frames loaded. Sample: {activeTab.data.grid[0]?.size} </div> )} {activeTab?.data?.history?.length > 0 && ( <div className="mt-4 text-xs text-gray-400"> <p className="mb-1">Export History:</p> <ul className="list-disc ml-4"> {activeTab.data.history.map((entry, idx) => ( <li key={idx}>{entry.time} — {entry.type.toUpperCase()}</li> ))} </ul> </div> )} {progress > 0 && ( <div className="mt-6"> <p className="text-sm mb-1 text-gray-400">{STAGES[progressStage]}</p> <div className="w-full h-3 bg-white/10 rounded-full overflow-hidden"> <div className="bg-[#7289DA] h-full transition-all duration-300" style={{ width: `${progress}%` }} /> </div> </div> )} <AnimatePresence> {notification && ( <motion.div initial={{ opacity: 0, y: 30, scale: 0.9 }} animate={{ opacity: 1, y: 0, scale: 1 }} exit={{ opacity: 0, y: 30, scale: 0.9 }} className="fixed bottom-6 right-6 bg-white/10 text-white border border-white/20 px-4 py-3 rounded-lg backdrop-blur"> <div className="flex items-center gap-2"> <Bell size={18} className="text-[#7289DA]" /> <span className="text-sm font-medium">{notification}</span> </div> </motion.div> )} </AnimatePresence> </div> ); }