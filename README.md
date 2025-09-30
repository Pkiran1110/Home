import React from 'react';

const HomePage = () => {
  return (
    <div>
      {/* Header */}
      <header style={styles.header}>
        <div style={styles.logo}>MyShop</div>
        <nav>
          <a href="/" style={styles.link}>Home</a>
          <a href="/products" style={styles.link}>Products</a>
          <a href="/cart" style={styles.link}>Cart</a>
          <a href="/login" style={styles.link}>Login</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section style={styles.hero}>
        <h1>Welcome to MyShop</h1>
        <p>Your one-stop shop for all things awesome.</p>
        <a href="/products" style={styles.shopBtn}>Shop Now</a>
      </section>

      {/* Categories Section */}
      <section style={styles.categories}>
        <h2>Featured Categories</h2>
        <div style={styles.categoryGrid}>
          {/* Add categories/components here as you build out */}
          <div style={styles.categoryCard}>Electronics</div>
          <div style={styles.categoryCard}>Fashion</div>
          <div style={styles.categoryCard}>Home & Living</div>
          <div style={styles.categoryCard}>Sports</div>
        </div>
      </section>

      {/* Footer */}
      <footer style={styles.footer}>
        <p>&copy; {new Date().getFullYear()} MyShop. All rights reserved.</p>
      </footer>
    </div>
  );
};

const styles = {
  header: {
    display: 'flex', justifyContent: 'space-between',
    alignItems: 'center', padding: '16px 32px', background: '#222', color: '#fff'
  },
  logo: { fontSize: '1.8rem', fontWeight: 'bold' },
  link: { color: '#fff', margin: '0 12px', textDecoration: 'none', fontSize: '1rem' },
  hero: {
    textAlign: 'center', padding: '100px 20px', background: '#fafafa'
  },
  shopBtn: {
    display: 'inline-block', marginTop: '20px', padding: '12px 32px',
    background: '#007bff', color: '#fff', borderRadius: '6px', textDecoration: 'none', fontSize: '1.2rem'
  },
  categories: { padding: '40px 20px', background: '#f5f5f5' },
  categoryGrid: {
    display: 'grid', gridTemplateColumns: 'repeat(4, 1fr)', gap: '24px', marginTop: '24px'
  },
  categoryCard: {
    background: '#fff', padding: '40px 0', textAlign: 'center',
    fontSize: '1.1rem', borderRadius: '8px', boxShadow: '0 1px 6px rgba(0,0,0,0.09)'
  },
  footer: {
    textAlign: 'center', padding: '16px', background: '#222', color: '#fff', marginTop: '40px'
  }
};

export default HomePage;
