  // Floating fire particles (only on pages that have a #particles field)
  const field = document.getElementById('particles');
  if(field){
    const n = window.innerWidth < 700 ? 14 : 26;
    for(let i=0;i<n;i++){
      const p = document.createElement('div');
      p.className='particle';
      const size = 2 + Math.random()*4;
      p.style.width=size+'px';p.style.height=size+'px';
      p.style.left = Math.random()*100+'%';
      p.style.setProperty('--drift', (Math.random()*80-40)+'px');
      p.style.animationDuration = (7+Math.random()*10)+'s';
      p.style.animationDelay = (Math.random()*10)+'s';
      field.appendChild(p);
    }
  }

  // Fade-up on scroll
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); } });
  },{threshold:0.15});
  document.querySelectorAll('.fade-up').forEach(el=>io.observe(el));

  // Header tint on scroll
  const header = document.querySelector('header');
  window.addEventListener('scroll', ()=>{
    header.style.background = window.scrollY>40 ? 'rgba(21,6,41,0.85)' : 'rgba(21,6,41,0.55)';
  });

  // Mobile menu toggle
  const burger = document.getElementById('burgerBtn');
  const navLinks = document.querySelector('.nav-links');
  burger.addEventListener('click', ()=>{
    const isOpen = navLinks.classList.toggle('open');
    burger.classList.toggle('open', isOpen);
    burger.setAttribute('aria-expanded', isOpen);
  });
  navLinks.querySelectorAll('a').forEach(a=>{
    a.addEventListener('click', ()=>{
      navLinks.classList.remove('open');
      burger.classList.remove('open');
      burger.setAttribute('aria-expanded','false');
    });
  });
