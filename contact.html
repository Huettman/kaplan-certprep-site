/* ═══════════════════════════════════════════════════════════════
   KAPLAN CERTPREP — Main JavaScript
   Handles: nav scroll, FAQ accordion, mobile nav, blog filters
   ═══════════════════════════════════════════════════════════════ */

// ─── NAV SCROLL EFFECT ────────────────────────────────────────
window.addEventListener('scroll', function() {
  const nav = document.querySelector('.nav');
  if (nav) {
    if (window.scrollY > 40) {
      nav.classList.add('nav--scrolled');
    } else {
      nav.classList.remove('nav--scrolled');
    }
  }
});

// ─── FAQ ACCORDION ────────────────────────────────────────────
document.addEventListener('DOMContentLoaded', function() {
  document.querySelectorAll('.faq-toggle').forEach(function(btn) {
    btn.addEventListener('click', function() {
      const item = this.closest('.faq-item');
      const wasOpen = item.classList.contains('open');
      // Close all
      document.querySelectorAll('.faq-item').forEach(function(el) {
        el.classList.remove('open');
      });
      // Toggle clicked
      if (!wasOpen) {
        item.classList.add('open');
      }
    });
  });
});

// ─── MOBILE NAV TOGGLE ───────────────────────────────────────
document.addEventListener('DOMContentLoaded', function() {
  const toggle = document.querySelector('.nav__mobile');
  const links = document.querySelector('.nav__links');
  if (toggle && links) {
    toggle.addEventListener('click', function() {
      const isVisible = links.style.display === 'flex';
      links.style.display = isVisible ? 'none' : 'flex';
      links.style.flexDirection = 'column';
      links.style.position = 'absolute';
      links.style.top = '64px';
      links.style.left = '0';
      links.style.right = '0';
      links.style.background = 'var(--purple)';
      links.style.padding = '16px 24px';
      links.style.gap = '16px';
    });
  }
});

// ─── BLOG FILTER & SEARCH ─────────────────────────────────────
document.addEventListener('DOMContentLoaded', function() {
  const filterChips = document.querySelectorAll('.filter-chip[data-cat]');
  const searchInput = document.querySelector('.blog-search');
  const blogCards = document.querySelectorAll('.blog-card[data-cat]');
  const paginationContainer = document.querySelector('.pagination');
  const blogGrid = document.querySelector('.blog-grid');
  
  if (!blogCards.length) return;

  const POSTS_PER_PAGE = 9;
  let currentCat = 'All';
  let currentSearch = '';
  let currentPage = 1;

  function getFiltered() {
    return Array.from(blogCards).filter(function(card) {
      const matchCat = currentCat === 'All' || card.dataset.cat === currentCat;
      const matchSearch = currentSearch === '' || 
        card.querySelector('.blog-card__title').textContent.toLowerCase().includes(currentSearch) ||
        card.querySelector('.blog-card__excerpt').textContent.toLowerCase().includes(currentSearch);
      return matchCat && matchSearch;
    });
  }

  function render() {
    const filtered = getFiltered();
    const totalPages = Math.ceil(filtered.length / POSTS_PER_PAGE);
    if (currentPage > totalPages) currentPage = 1;
    
    const start = (currentPage - 1) * POSTS_PER_PAGE;
    const end = start + POSTS_PER_PAGE;

    // Show/hide cards
    blogCards.forEach(function(card) { card.style.display = 'none'; });
    filtered.slice(start, end).forEach(function(card) { card.style.display = 'block'; });

    // Update pagination
    if (paginationContainer && totalPages > 1) {
      let html = '';
      if (currentPage > 1) {
        html += '<button class="pagination__btn" data-page="' + (currentPage-1) + '">← Prev</button>';
      }
      for (var i = 1; i <= totalPages; i++) {
        html += '<button class="pagination__btn' + (i === currentPage ? ' active' : '') + '" data-page="' + i + '">' + i + '</button>';
      }
      if (currentPage < totalPages) {
        html += '<button class="pagination__btn" data-page="' + (currentPage+1) + '">Next →</button>';
      }
      html += '<div class="pagination__info" style="width:100%;text-align:center">Showing ' + (start+1) + '–' + Math.min(end, filtered.length) + ' of ' + filtered.length + ' articles</div>';
      paginationContainer.innerHTML = html;

      // Rebind pagination clicks
      paginationContainer.querySelectorAll('.pagination__btn').forEach(function(btn) {
        btn.addEventListener('click', function() {
          currentPage = parseInt(this.dataset.page);
          render();
          window.scrollTo({ top: blogGrid.offsetTop - 100, behavior: 'smooth' });
        });
      });
    } else if (paginationContainer) {
      paginationContainer.innerHTML = '';
    }
  }

  // Filter chip clicks
  filterChips.forEach(function(chip) {
    chip.addEventListener('click', function() {
      filterChips.forEach(function(c) { c.classList.remove('active'); });
      this.classList.add('active');
      currentCat = this.dataset.cat;
      currentPage = 1;
      render();
    });
  });

  // Search input
  if (searchInput) {
    searchInput.addEventListener('input', function() {
      currentSearch = this.value.toLowerCase();
      currentPage = 1;
      render();
    });
  }

  // Initial render
  render();
});

// ─── FADE-IN ON SCROLL ────────────────────────────────────────
document.addEventListener('DOMContentLoaded', function() {
  const observer = new IntersectionObserver(function(entries) {
    entries.forEach(function(entry) {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.fade-in').forEach(function(el) {
    observer.observe(el);
  });
});
