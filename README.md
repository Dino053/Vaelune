export default function VaeluneWebsite() {
  const products = [
    {
      name: 'LUNARIS Hoodie',
      price: '€89',
      image:
        'https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?q=80&w=1200&auto=format&fit=crop',
    },
    {
      name: 'ECLIPSE Tee',
      price: '€49',
      image:
        'https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?q=80&w=1200&auto=format&fit=crop',
    },
    {
      name: 'NOCTURNE Pants',
      price: '€79',
      image:
        'https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?q=80&w=1200&auto=format&fit=crop',
    },
  ]

  return (
    <div className="min-h-screen bg-black text-white font-sans">
      {/* HERO */}
      <section className="relative h-screen flex items-center justify-center overflow-hidden">
        <img
          src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?q=80&w=1800&auto=format&fit=crop"
          alt="Vaelune Hero"
          className="absolute inset-0 w-full h-full object-cover opacity-30"
        />

        <div className="absolute inset-0 bg-gradient-to-b from-black/40 via-black/60 to-black"></div>

        <div className="relative z-10 text-center px-6 max-w-4xl">
          <p className="tracking-[0.4em] text-sm uppercase text-gray-300 mb-4">
            Beyond The Light
          </p>

          <h1 className="text-6xl md:text-8xl font-light tracking-[0.3em] mb-6">
            VAELUNE
          </h1>

          <p className="text-gray-300 text-lg md:text-xl max-w-2xl mx-auto leading-relaxed">
            Une marque indépendante inspirée par la lune, l’ombre et l’élégance.
            Des pièces minimalistes pensées pour une nouvelle génération.
          </p>

          <div className="mt-10 flex gap-4 justify-center flex-wrap">
            <button className="px-8 py-4 bg-white text-black rounded-2xl font-medium hover:scale-105 transition">
              Acheter
            </button>

            <button className="px-8 py-4 border border-white/30 rounded-2xl hover:bg-white/10 transition">
              Découvrir
            </button>
          </div>
        </div>
      </section>

      {/* ABOUT */}
      <section className="py-28 px-6 md:px-20 border-t border-white/10">
        <div className="grid md:grid-cols-2 gap-16 items-center">
          <div>
            <p className="uppercase tracking-[0.3em] text-gray-400 mb-4 text-sm">
              Notre univers
            </p>

            <h2 className="text-4xl md:text-5xl font-light mb-8 leading-tight">
              Entre mystère et modernité.
            </h2>

            <p className="text-gray-300 leading-relaxed text-lg">
              Vaelune mélange le streetwear premium avec une esthétique sombre et
              céleste. Chaque collection représente un équilibre entre lumière,
              minimalisme et identité forte.
            </p>
          </div>

          <div>
            <img
              src="https://images.unsplash.com/photo-1496747611176-843222e1e57c?q=80&w=1200&auto=format&fit=crop"
              alt="Vaelune Fashion"
              className="rounded-3xl shadow-2xl object-cover h-[600px] w-full"
            />
          </div>
        </div>
      </section>

      {/* COLLECTION */}
      <section className="py-28 px-6 md:px-20 bg-zinc-950 border-t border-white/10">
        <div className="flex items-end justify-between flex-wrap gap-4 mb-16">
          <div>
            <p className="uppercase tracking-[0.3em] text-gray-400 mb-4 text-sm">
              Collection
            </p>

            <h2 className="text-4xl md:text-5xl font-light">
              Pièces signature
            </h2>
          </div>

          <button className="border border-white/20 px-6 py-3 rounded-2xl hover:bg-white hover:text-black transition">
            Voir toute la boutique
          </button>
        </div>

        <div className="grid md:grid-cols-3 gap-8">
          {products.map((product, index) => (
            <div
              key={index}
              className="group bg-black rounded-3xl overflow-hidden border border-white/10 hover:border-white/30 transition"
            >
              <div className="overflow-hidden">
                <img
                  src={product.image}
                  alt={product.name}
                  className="h-[500px] w-full object-cover group-hover:scale-105 transition duration-500"
                />
              </div>

              <div className="p-6">
                <div className="flex items-center justify-between">
                  <div>
                    <h3 className="text-2xl font-light">{product.name}</h3>
                    <p className="text-gray-400 mt-2">Edition limitée</p>
                  </div>

                  <p className="text-xl">{product.price}</p>
                </div>

                <button className="mt-6 w-full bg-white text-black py-4 rounded-2xl font-medium hover:opacity-90 transition">
                  Ajouter au panier
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* LOOKBOOK */}
      <section className="py-28 px-6 md:px-20 border-t border-white/10">
        <div className="text-center mb-16">
          <p className="uppercase tracking-[0.3em] text-gray-400 mb-4 text-sm">
            Lookbook
          </p>

          <h2 className="text-4xl md:text-5xl font-light">
            Beyond the light.
          </h2>
        </div>

        <div className="grid md:grid-cols-3 gap-6">
          <img
            src="https://images.unsplash.com/photo-1529139574466-a303027c1d8b?q=80&w=1200&auto=format&fit=crop"
            className="rounded-3xl h-[500px] object-cover w-full"
          />

          <img
            src="https://images.unsplash.com/photo-1495385794356-15371f348c31?q=80&w=1200&auto=format&fit=crop"
            className="rounded-3xl h-[500px] object-cover w-full"
          />

          <img
            src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?q=80&w=1200&auto=format&fit=crop"
            className="rounded-3xl h-[500px] object-cover w-full"
          />
        </div>
      </section>

      {/* NEWSLETTER */}
      <section className="py-28 px-6 md:px-20 bg-zinc-950 border-t border-white/10 text-center">
        <p className="uppercase tracking-[0.3em] text-gray-400 mb-4 text-sm">
          Rejoins Vaelune
        </p>

        <h2 className="text-4xl md:text-6xl font-light mb-8">
          Accès exclusif aux prochaines collections.
        </h2>

        <div className="max-w-xl mx-auto flex flex-col md:flex-row gap-4">
          <input
            type="email"
            placeholder="Votre email"
            className="flex-1 bg-black border border-white/10 rounded-2xl px-6 py-4 outline-none"
          />

          <button className="bg-white text-black px-8 py-4 rounded-2xl font-medium hover:opacity-90 transition">
            S’inscrire
          </button>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="border-t border-white/10 py-10 px-6 md:px-20 flex flex-col md:flex-row justify-between gap-6 text-gray-400">
        <div>
          <h3 className="text-white tracking-[0.3em] text-xl mb-2">VAELUNE</h3>
          <p>Independent Fashion Brand</p>
        </div>

        <div className="flex gap-6">
          <a href="#" className="hover:text-white transition">
            Instagram
          </a>
          <a href="#" className="hover:text-white transition">
            TikTok
          </a>
          <a href="#" className="hover:text-white transition">
            Contact
          </a>
        </div>
      </footer>
    </div>
  )
}
