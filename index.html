import React, { useState, useEffect, useRef } from 'react';
import { User, Camera, MessageCircle, Search, Zap, Shield, Lock, Unlock, ChevronLeft, Send, Globe, Sparkles, Scan, X, CheckCircle, Activity, Eye, Fingerprint, Menu } from 'lucide-react';

// --- ASSETS & DATA ---
const MY_PROFILE = {
  name: "You",
  image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=600&h=600&fit=crop&q=80",
};

const MOCK_DOPPELGANGS = [
  {
    id: 1,
    name: "Marcus R.",
    age: 26,
    location: "Berlin",
    matchScore: 98,
    isPrivate: false,
    image: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=600&h=600&fit=crop&q=80",
    bio: "Found this app because my friends keep confusing me for someone else."
  },
  {
    id: 2,
    name: "Unknown User",
    age: 27,
    location: "Toronto",
    matchScore: 94,
    isPrivate: true, 
    image: "https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?w=600&h=600&fit=crop&q=80",
    avatar: "https://api.dicebear.com/9.x/micah/svg?seed=Marcus&backgroundColor=b6e3f4", 
    bio: "I'm keeping it a mystery. 94% match? Prove it."
  },
  {
    id: 3,
    name: "Liam T.",
    age: 25,
    location: "Austin",
    matchScore: 82,
    isPrivate: false,
    image: "https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?w=600&h=600&fit=crop&q=80",
    bio: "Looking for my twin."
  },
  {
    id: 5,
    name: "Koji",
    age: 24,
    location: "Tokyo",
    matchScore: 64,
    isPrivate: true,
    image: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=600&h=600&fit=crop&q=80",
    avatar: "https://api.dicebear.com/9.x/micah/svg?seed=Sarah&backgroundColor=ffdfbf", 
    bio: "Maybe we are distant cousins?"
  }
];

const SEARCH_RESULTS = [
    { id: 101, name: "Sarah Jenkins", image: "https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=400&h=400&fit=crop", match: 12, username: "@sarahj" },
    { id: 102, name: "Sarah Ma", image: "https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=400&h=400&fit=crop", match: 45, username: "@s_ma" },
    { id: 103, name: "Sara K.", image: "https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=400&h=400&fit=crop", match: 89, username: "@sarak" },
    { id: 104, name: "Sam Smith", image: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=400&h=400&fit=crop", match: 92, username: "@sammy" }
];

// --- UTILS ---
const getScoreColor = (score) => {
  if (score >= 90) return 'text-emerald-400 drop-shadow-[0_0_8px_rgba(52,211,153,0.8)]';
  if (score >= 70) return 'text-cyan-400 drop-shadow-[0_0_8px_rgba(34,211,238,0.8)]';
  return 'text-rose-400 drop-shadow-[0_0_8px_rgba(251,113,133,0.8)]';
};

// --- COMPONENTS ---

export default function App() {
  const [view, setView] = useState('onboarding'); 
  const [selectedUser, setSelectedUser] = useState(null);
  const [connected, setConnected] = useState([]);

  const transitionTo = (newView) => setView(newView);

  // --- ONBOARDING ---
  const Onboarding = () => (
    <div className="h-full flex flex-col relative overflow-hidden bg-black">
      <div className="absolute top-[-20%] left-[-20%] w-[140%] h-[140%] bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-emerald-900/40 via-black to-black animate-pulse-slow"></div>
      <div className="absolute inset-0 bg-[url('https://grainy-gradients.vercel.app/noise.svg')] opacity-20 mix-blend-overlay"></div>
      <div className="relative z-10 flex-1 flex flex-col justify-end p-8 pb-12 space-y-8">
        <div className="space-y-2">
          <div className="inline-flex items-center gap-2 px-3 py-1 rounded-full border border-emerald-500/30 bg-emerald-500/10 text-emerald-400 text-xs font-medium tracking-wider uppercase mb-4 backdrop-blur-md">
            <Sparkles size={12} /> Beta Access
          </div>
          <h1 className="text-6xl font-black tracking-tighter text-white leading-[0.9]">
            Doppel<br/><span className="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-cyan-400">gang.</span>
          </h1>
          <p className="text-gray-400 text-lg max-w-[80%] leading-relaxed">
            There is a 50% chance your exact lookalike is out there. Let's find them.
          </p>
        </div>
        <button onClick={() => transitionTo('scan')} className="group relative w-full py-5 bg-white text-black font-bold text-lg rounded-2xl overflow-hidden transition-transform active:scale-95">
          <div className="absolute inset-0 bg-gradient-to-r from-emerald-200 via-white to-cyan-200 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          <span className="relative z-10 flex items-center justify-center gap-2">Connect with FaceID <Scan size={20} /></span>
        </button>
      </div>
    </div>
  );

  // --- REDESIGNED MODERN SCAN VIEW ---
  const ScanView = () => {
    const [state, setState] = useState('scanning'); // scanning, verified

    useEffect(() => {
      // Sequence: 
      // 0s: Start Scan
      // 2.5s: Verified (Green)
      // 3.5s: Redirect
      
      const timer1 = setTimeout(() => setState('verified'), 2500);
      const timer2 = setTimeout(() => transitionTo('home'), 3500);

      return () => {
        clearTimeout(timer1);
        clearTimeout(timer2);
      };
    }, []);

    return (
      <div className="h-full bg-black flex flex-col items-center justify-center relative overflow-hidden">
        {/* Background with dark mesh */}
        <div className="absolute inset-0 bg-[radial-gradient(circle_at_center,_#10b981_0%,_#000_40%)] opacity-10 animate-pulse"></div>
        <div className="absolute inset-0 bg-[linear-gradient(to_right,#80808012_1px,transparent_1px),linear-gradient(to_bottom,#80808012_1px,transparent_1px)] bg-[size:24px_24px]"></div>

        <div className="relative z-10 flex flex-col items-center">
            {/* The Scanner Container */}
            <div className="relative w-64 h-64 mb-8">
                
                {/* 1. The Rotating Rings (Modern Target) */}
                <div className={`absolute inset-0 rounded-full border border-emerald-500/30 border-t-emerald-500 border-r-transparent transition-all duration-700 ease-out ${state === 'verified' ? 'rotate-0 scale-105 border-emerald-500' : 'animate-spin-slow'}`}></div>
                <div className={`absolute inset-4 rounded-full border border-emerald-500/20 border-b-emerald-500 border-l-transparent transition-all duration-700 ease-out ${state === 'verified' ? 'rotate-0 scale-100 border-emerald-500' : 'animate-spin-reverse-slow'}`}></div>

                {/* 2. User Image with Effects */}
                <div className="absolute inset-8 rounded-full overflow-hidden border-2 border-emerald-900/50 relative bg-black">
                    <img 
                        src={MY_PROFILE.image} 
                        className={`w-full h-full object-cover transition-all duration-1000 ${state === 'verified' ? 'opacity-100 grayscale-0 scale-100' : 'opacity-60 grayscale scale-110 blur-sm'}`} 
                    />
                    
                    {/* Scanning Beam (Only while scanning) */}
                    {state === 'scanning' && (
                        <div className="absolute top-0 left-0 w-full h-full bg-gradient-to-b from-transparent via-emerald-500/30 to-transparent animate-scan-fast mix-blend-overlay"></div>
                    )}

                    {/* Success Flash Overlay */}
                    <div className={`absolute inset-0 bg-emerald-500/20 transition-opacity duration-300 ${state === 'verified' ? 'opacity-100' : 'opacity-0'}`}></div>
                </div>

                {/* 3. Success Icon */}
                <div className={`absolute inset-0 flex items-center justify-center transition-all duration-500 transform ${state === 'verified' ? 'scale-100 opacity-100' : 'scale-50 opacity-0'}`}>
                    <div className="bg-black rounded-full p-2 border border-emerald-500 shadow-[0_0_30px_rgba(16,185,129,0.6)]">
                         <CheckCircle className="text-emerald-400 w-12 h-12 fill-emerald-900/50" />
                    </div>
                </div>
            </div>

            {/* Text Status */}
            <div className="h-12 flex flex-col items-center justify-center">
                {state === 'scanning' ? (
                    <div className="flex flex-col items-center space-y-2">
                         <div className="flex gap-1">
                            <div className="w-1.5 h-1.5 bg-emerald-500 rounded-full animate-bounce"></div>
                            <div className="w-1.5 h-1.5 bg-emerald-500 rounded-full animate-bounce delay-100"></div>
                            <div className="w-1.5 h-1.5 bg-emerald-500 rounded-full animate-bounce delay-200"></div>
                         </div>
                         <span className="text-emerald-500/70 font-mono text-xs tracking-[0.3em] uppercase">Biometric Sync</span>
                    </div>
                ) : (
                    <div className="text-emerald-400 font-bold text-lg tracking-widest animate-pulse">
                        IDENTITY VERIFIED
                    </div>
                )}
            </div>
        </div>
      </div>
    );
  };

  // --- HOME FEED ---
  const Home = () => (
    <div className="h-full bg-black text-white relative overflow-y-auto pb-24 scrollbar-hide">
      <div className="sticky top-0 z-20 px-6 py-5 flex justify-between items-end bg-gradient-to-b from-black via-black/90 to-transparent backdrop-blur-md">
        <div>
          <div className="text-white/40 text-xs font-bold tracking-widest uppercase mb-1">Discover</div>
          <h2 className="text-2xl font-bold tracking-tight">Your Matches</h2>
        </div>
        <div className="w-10 h-10 rounded-full border-2 border-emerald-500/30 overflow-hidden p-0.5">
          <img src={MY_PROFILE.image} className="w-full h-full object-cover rounded-full" />
        </div>
      </div>

      <div className="px-4 space-y-4 mt-2">
        {MOCK_DOPPELGANGS.map((user) => (
          <div 
            key={user.id}
            onClick={() => { setSelectedUser(user); transitionTo('profile'); }}
            className="group relative w-full aspect-[4/5] rounded-[2rem] overflow-hidden bg-gray-900 cursor-pointer active:scale-[0.98] transition-all duration-300 border border-white/10 shadow-2xl"
          >
            <img 
              src={user.isPrivate && !connected.includes(user.id) ? user.avatar : user.image} 
              className={`w-full h-full object-cover transition-transform duration-700 group-hover:scale-105 ${user.isPrivate && !connected.includes(user.id) ? 'p-12 bg-[#e0f2fe]' : ''}`}
            />
            <div className="absolute inset-0 bg-gradient-to-t from-black via-black/40 to-transparent opacity-90"></div>
            
            <div className="absolute top-4 right-4 bg-black/60 backdrop-blur-md border border-white/10 rounded-full px-3 py-1 flex items-center gap-1">
              <Zap size={12} className={getScoreColor(user.matchScore).split(' ')[0]} fill="currentColor" />
              <span className={`font-bold font-mono ${getScoreColor(user.matchScore)}`}>{user.matchScore}%</span>
            </div>

            {user.isPrivate && !connected.includes(user.id) && (
               <div className="absolute top-4 left-4 bg-indigo-500/20 backdrop-blur-md border border-indigo-500/30 rounded-full px-3 py-1 flex items-center gap-1 text-indigo-200 text-xs font-bold uppercase tracking-wide">
                 <Shield size={10} /> Private
               </div>
            )}

            <div className="absolute bottom-0 left-0 w-full p-6">
               <h3 className="text-3xl font-bold text-white mb-1">{user.name}, {user.age}</h3>
               <div className="flex items-center gap-2 text-white/60 text-sm font-medium">
                 <Globe size={14} /> {user.location}
               </div>
            </div>
          </div>
        ))}
      </div>
    </div>
  );

  // --- PROFILE (Fixed Crash) ---
  const Profile = () => {
    // Safety check: If no user selected, show Home
    if (!selectedUser) {
        setTimeout(() => transitionTo('home'), 0);
        return <div className="h-full bg-black flex items-center justify-center"><Activity className="animate-spin text-emerald-500"/></div>;
    }

    const isFriend = connected.includes(selectedUser.id);
    const reveal = !selectedUser.isPrivate || isFriend;

    return (
      <div className="h-full bg-black flex flex-col relative">
        <div className="relative flex-1 overflow-hidden">
          <img 
            src={reveal ? selectedUser.image : selectedUser.avatar}
            className={`absolute inset-0 w-full h-full object-cover ${!reveal ? 'p-12 bg-[#e0f2fe]' : ''}`}
          />
          <div className="absolute inset-0 bg-gradient-to-t from-black via-black/20 to-transparent"></div>
          
          <div className="absolute top-0 left-0 w-full p-4 flex justify-between items-center z-20">
            <button onClick={() => transitionTo('home')} className="w-10 h-10 bg-black/20 backdrop-blur-md rounded-full flex items-center justify-center text-white border border-white/10 hover:bg-white/10 transition">
              <ChevronLeft />
            </button>
          </div>
          
          <div className="absolute bottom-0 w-full p-8 pb-32 space-y-6 z-20">
             <div className="inline-flex items-center gap-2 bg-black/60 backdrop-blur-xl px-4 py-2 rounded-full border border-white/10">
                <span className="text-white/60 text-xs font-bold uppercase tracking-wider">Resemblance</span>
                <span className={`text-xl font-black font-mono ${getScoreColor(selectedUser.matchScore)}`}>{selectedUser.matchScore}%</span>
             </div>

             <div>
               <h1 className="text-4xl font-bold text-white mb-2">{selectedUser.name}, {selectedUser.age}</h1>
               <p className="text-lg text-white/80 leading-relaxed font-light">{selectedUser.bio}</p>
             </div>

             {!reveal && (
               <div className="bg-indigo-900/40 backdrop-blur-md border border-indigo-500/30 p-4 rounded-xl flex gap-4 items-center">
                  <div className="w-10 h-10 rounded-full bg-indigo-500/20 flex items-center justify-center text-indigo-300 shrink-0">
                    <Lock size={20} />
                  </div>
                  <div className="text-sm text-indigo-100">
                    <span className="font-bold text-white">Identity Hidden.</span> Connect to reveal face.
                  </div>
               </div>
             )}
          </div>
        </div>

        <div className="absolute bottom-8 left-0 w-full px-8 z-30">
          {isFriend ? (
            <button 
              onClick={() => transitionTo('chat_direct')}
              className="w-full py-4 bg-emerald-500 hover:bg-emerald-400 text-black font-bold rounded-2xl shadow-[0_0_20px_rgba(16,185,129,0.4)] transition-all flex items-center justify-center gap-2"
            >
              <MessageCircle /> Open Chat
            </button>
          ) : (
            <button 
              onClick={() => setConnected([...connected, selectedUser.id])}
              className="w-full py-4 bg-white hover:bg-gray-100 text-black font-bold rounded-2xl shadow-xl transition-all flex items-center justify-center gap-2"
            >
              {selectedUser.isPrivate ? <Unlock size={20} /> : <User size={20} />}
              {selectedUser.isPrivate ? "Connect & Reveal Face" : "Connect"}
            </button>
          )}
        </div>
      </div>
    );
  };

  // --- MESSAGES LIST (New) ---
  const MessagesList = () => (
     <div className="h-full bg-black flex flex-col p-6">
         <h2 className="text-3xl font-bold text-white mb-6">Messages</h2>
         <div className="space-y-4">
             {connected.length === 0 ? (
                 <div className="text-center text-gray-500 mt-20">
                     <MessageCircle size={48} className="mx-auto mb-4 opacity-50"/>
                     <p>No connections yet.</p>
                     <p className="text-sm">Connect with matches to start chatting.</p>
                 </div>
             ) : (
                 // Filter only connected users
                 MOCK_DOPPELGANGS.filter(u => connected.includes(u.id)).map(u => (
                     <div key={u.id} onClick={() => { setSelectedUser(u); transitionTo('chat_direct'); }} className="flex items-center gap-4 p-4 bg-gray-900 rounded-2xl border border-white/5 hover:bg-gray-800 cursor-pointer">
                         <div className="w-12 h-12 rounded-full overflow-hidden">
                             <img src={u.image} className="w-full h-full object-cover" />
                         </div>
                         <div className="flex-1">
                             <div className="font-bold text-white">{u.name}</div>
                             <div className="text-xs text-gray-400">Tap to chat</div>
                         </div>
                         <ChevronRight className="text-gray-600" />
                     </div>
                 ))
             )}
         </div>
     </div>
  );

  // --- DIRECT CHAT (Fixed Crash) ---
  const ChatDirect = () => {
    if (!selectedUser) {
        setTimeout(() => transitionTo('messages'), 0);
        return null;
    }
    
    const [input, setInput] = useState("");
    const [msgs, setMsgs] = useState([
        { id: 1, sender: 'them', text: "Wait, are you actually in Berlin too?" },
        { id: 2, sender: 'me', text: "Yeah! I'm near Mitte." }
    ]);

    const send = () => {
        if (!input.trim()) return;
        setMsgs([...msgs, { id: Date.now(), sender: 'me', text: input }]);
        setInput("");
    };

    return (
     <div className="h-full bg-black flex flex-col relative">
        <div className="pt-6 pb-4 px-4 border-b border-white/10 bg-black/50 backdrop-blur-md flex items-center gap-4">
          <button onClick={() => transitionTo('messages')} className="p-2 text-white/50 hover:text-white transition"><ChevronLeft /></button>
          <div className="w-10 h-10 rounded-full overflow-hidden border border-white/20">
            <img src={selectedUser.image} className="w-full h-full object-cover" />
          </div>
          <div>
            <div className="text-white font-bold text-lg">{selectedUser.name}</div>
            <div className="text-emerald-400 text-xs flex items-center gap-1"><div className="w-2 h-2 rounded-full bg-emerald-500"></div> Online</div>
          </div>
        </div>

        <div className="flex-1 p-4 space-y-6 overflow-y-auto">
          <div className="text-center text-white/20 text-xs uppercase tracking-widest my-4">Today</div>
          {msgs.map(m => (
              <div key={m.id} className={`flex gap-3 items-end ${m.sender === 'me' ? 'justify-end' : ''}`}>
                  {m.sender === 'them' && <div className="w-8 h-8 rounded-full overflow-hidden bg-gray-800 shrink-0"><img src={selectedUser.image} className="w-full h-full object-cover" /></div>}
                  <div className={`${m.sender === 'me' ? 'bg-emerald-600 text-white rounded-br-none' : 'bg-[#222] text-gray-200 rounded-bl-none'} px-5 py-3 rounded-2xl max-w-[75%] leading-relaxed border border-white/5`}>
                      {m.text}
                  </div>
              </div>
          ))}
        </div>

        <div className="p-4 pb-8 bg-black border-t border-white/10">
          <div className="bg-[#1a1a1a] rounded-full p-1 pl-5 flex items-center border border-white/10 focus-within:border-emerald-500/50 transition-colors">
            <input 
                type="text" 
                value={input}
                onChange={e => setInput(e.target.value)}
                onKeyDown={e => e.key === 'Enter' && send()}
                placeholder="Message..." 
                className="bg-transparent flex-1 text-white outline-none placeholder:text-gray-600 h-10" 
            />
            <button onClick={send} className="w-10 h-10 bg-[#333] hover:bg-emerald-500 hover:text-black text-white rounded-full flex items-center justify-center transition-all">
              <Send size={18} />
            </button>
          </div>
        </div>
     </div>
    );
  };

  const Compare = () => {
    const [query, setQuery] = useState('');
    const [compareResult, setCompareResult] = useState(null); 
    const [animationState, setAnimationState] = useState('idle'); 

    const filteredUsers = query.length > 0 
        ? SEARCH_RESULTS.filter(u => u.name.toLowerCase().includes(query.toLowerCase()))
        : [];

    const handleSelect = (user) => {
        setQuery('');
        setAnimationState('scanning');
        setCompareResult(null);
        setTimeout(() => {
            setAnimationState('result');
            setCompareResult({ user, score: user.match });
        }, 2500);
    };

    return (
      <div className="h-full bg-black flex flex-col relative overflow-hidden">
        {animationState === 'idle' && (
            <div className="flex-col flex h-full">
                <div className="pt-8 px-6 pb-4 bg-gradient-to-b from-black via-black to-transparent z-10">
                    <h2 className="text-3xl font-bold text-white mb-6">Search</h2>
                    <div className="relative">
                        <Search className="absolute left-4 top-3.5 text-gray-500" size={20} />
                        <input 
                            type="text" 
                            placeholder="Search users (e.g. Sarah)" 
                            value={query}
                            onChange={e => setQuery(e.target.value)}
                            className="w-full bg-[#1a1a1a] border border-white/10 rounded-2xl py-3 pl-12 pr-4 text-white focus:outline-none focus:border-emerald-500/50 transition-all placeholder:text-gray-600"
                        />
                    </div>
                </div>

                <div className="flex-1 overflow-y-auto px-6 pb-24">
                    {query.length === 0 ? (
                        <div className="text-center mt-20 space-y-4 opacity-30">
                            <Search className="w-12 h-12 mx-auto" />
                            <p className="text-sm">Search for a specific user to see your match score with them.</p>
                        </div>
                    ) : (
                        <div className="space-y-3">
                            {filteredUsers.map(u => (
                                <div key={u.id} onClick={() => handleSelect(u)} className="flex items-center gap-4 p-3 bg-[#111] rounded-2xl border border-white/5 hover:bg-[#222] active:scale-[0.98] transition-all cursor-pointer">
                                    <div className="w-12 h-12 rounded-full bg-gray-800 overflow-hidden"><img src={u.image} className="w-full h-full object-cover" /></div>
                                    <div className="flex-1"><div className="font-bold text-white">{u.name}</div><div className="text-xs text-gray-500">{u.username}</div></div>
                                    <div className="w-8 h-8 rounded-full border border-white/10 flex items-center justify-center text-emerald-500"><Scan size={14} /></div>
                                </div>
                            ))}
                        </div>
                    )}
                </div>
            </div>
        )}

        {animationState !== 'idle' && (
            <div className="absolute inset-0 bg-black z-50 flex flex-col">
                 <button onClick={() => setAnimationState('idle')} className="absolute top-6 left-6 z-50 text-white/50 hover:text-white p-2 bg-black/20 backdrop-blur-md rounded-full"><X size={24} /></button>
                 <div className="flex-1 flex flex-col items-center justify-center relative">
                    <div className="absolute inset-0 bg-[radial-gradient(circle_at_center,_#064e3b_0%,_#000_70%)] opacity-50"></div>
                    <div className="flex items-center gap-4 relative z-10 mb-12">
                        <div className="w-28 h-28 rounded-full border-4 border-white/10 overflow-hidden relative"><img src={MY_PROFILE.image} className="w-full h-full object-cover opacity-80" /></div>
                        <div className="w-10 h-10 rounded-full bg-black border border-white/20 flex items-center justify-center font-black text-xs italic shadow-xl z-20 relative">VS</div>
                        <div className="w-28 h-28 rounded-full border-4 border-white/10 overflow-hidden relative">
                            {compareResult ? <img src={compareResult.user.image} className="w-full h-full object-cover" /> : <div className="w-full h-full bg-gray-800 animate-pulse"></div>}
                        </div>
                         {animationState === 'scanning' && <div className="absolute top-0 left-0 w-full h-full bg-gradient-to-b from-emerald-500/0 via-emerald-500/50 to-emerald-500/0 animate-scan z-30 pointer-events-none mix-blend-screen"></div>}
                    </div>
                    <div className="text-center z-10 h-24">
                        {animationState === 'scanning' ? <div className="text-emerald-400 font-mono text-sm tracking-[0.2em] animate-pulse">COMPARING FEATURES...</div> : (
                             <div className="animate-bounce">
                                <div className="text-sm text-gray-400 uppercase tracking-widest mb-2">Match Score</div>
                                <div className={`text-7xl font-black font-mono ${getScoreColor(compareResult.score)}`}>{compareResult.score}%</div>
                             </div>
                        )}
                    </div>
                 </div>
            </div>
        )}
      </div>
    );
  }

  // --- MY PROFILE VIEW ---
  const MyProfile = () => (
      <div className="h-full bg-black flex flex-col p-8 text-center items-center justify-center space-y-6">
          <div className="w-32 h-32 rounded-full border-4 border-emerald-500/20 overflow-hidden relative group">
              <img src={MY_PROFILE.image} className="w-full h-full object-cover" />
              <div className="absolute inset-0 bg-black/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition cursor-pointer">
                  <Camera className="text-white"/>
              </div>
          </div>
          <div>
              <h2 className="text-2xl font-bold text-white">{MY_PROFILE.name}</h2>
              <p className="text-gray-500">Free Account</p>
          </div>
          <div className="w-full bg-gray-900 rounded-xl p-4 border border-white/10">
              <div className="flex justify-between text-sm text-gray-400 mb-2"><span>Profile Complete</span><span>80%</span></div>
              <div className="w-full h-2 bg-gray-800 rounded-full overflow-hidden"><div className="h-full w-[80%] bg-emerald-500"></div></div>
          </div>
          <button onClick={() => transitionTo('onboarding')} className="text-red-500 text-sm mt-8">Log Out</button>
      </div>
  );

  // --- NAV DOCK ---
  const Dock = () => (
    <div className="absolute bottom-6 left-1/2 -translate-x-1/2 bg-white/10 backdrop-blur-xl border border-white/10 p-2 rounded-full flex items-center gap-1 shadow-2xl z-40">
      {[
        { id: 'home', icon: Sparkles },
        { id: 'compare', icon: Search },
        { id: 'messages', icon: MessageCircle },
        { id: 'my_profile', icon: User }
      ].map((item) => (
        <button 
          key={item.id}
          onClick={() => transitionTo(item.id)}
          className={`p-3 rounded-full transition-all duration-300 ${view === item.id || (view === 'chat_direct' && item.id === 'messages') ? 'bg-white text-black shadow-lg scale-110' : 'text-white/50 hover:bg-white/10'}`}
        >
          <item.icon size={20} />
        </button>
      ))}
    </div>
  );

  // --- ROOT ---
  return (
    <div className="flex justify-center items-center min-h-screen bg-[#050505] font-sans text-white selection:bg-emerald-500/30">
      <div className="w-full max-w-md h-[100dvh] md:h-[850px] bg-black md:rounded-[40px] shadow-[0_0_50px_rgba(255,255,255,0.05)] overflow-hidden relative flex flex-col border-[6px] border-[#1a1a1a]">
        <div className="flex-1 relative overflow-hidden">
          {view === 'onboarding' && <Onboarding />}
          {view === 'scan' && <ScanView />}
          {view === 'home' && <Home />}
          {view === 'profile' && <Profile />}
          {view === 'messages' && <MessagesList />}
          {view === 'chat_direct' && <ChatDirect />}
          {view === 'compare' && <Compare />}
          {view === 'my_profile' && <MyProfile />}
        </div>
        {['home', 'compare', 'messages', 'chat_direct', 'my_profile', 'profile'].includes(view) && <Dock />}
      </div>
      <style>{`
        @keyframes scan {
          0% { top: 0%; opacity: 0; }
          5% { opacity: 1; }
          90% { opacity: 1; }
          100% { top: 100%; opacity: 0; }
        }
        .animate-scan {
          animation: scan 2s cubic-bezier(0.4, 0, 0.2, 1) infinite;
        }
        
        @keyframes scan-fast {
           0% { top: -100%; }
           100% { top: 200%; }
        }
        .animate-scan-fast {
            animation: scan-fast 1.5s cubic-bezier(0.4, 0, 0.2, 1) infinite;
        }

        .animate-spin-slow {
            animation: spin 4s linear infinite;
        }
        .animate-spin-reverse-slow {
            animation: spin 6s linear infinite reverse;
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .scrollbar-hide::-webkit-scrollbar { display: none; }
        .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }
      `}</style>
    </div>
  );
}
