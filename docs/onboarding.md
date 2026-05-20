# Hachi Studio — Client Onboarding

## What to collect from the client (via WhatsApp)

Send this checklist after they pay:

```
¡Perfecto [Nombre]! 🎉 Empezamos ahora mismo.

Para tener tu página lista en 48 horas necesito que me envíes:

📋 INFORMACIÓN BÁSICA
□ Nombre de tu negocio (como quieres que aparezca)
□ Slogan o frase corta (opcional)
□ Dirección completa
□ Número de WhatsApp (puede ser el mismo que usamos)
□ Horarios de atención (ej: Lunes-Viernes 8am-6pm)
□ Ciudad y barrio

📸 FOTOS (mínimo 3, máximo 10)
□ Logo (PNG con fondo transparente, o JPG de buena calidad)
□ Foto de portada (tu negocio, tus instalaciones, o una mascota bien bonita)
□ Fotos de tu equipo o instalaciones
□ Fotos de trabajos realizados (antes/después, mascotas atendidas)

🛠 SERVICIOS
□ Lista de servicios con precio (ej: "Baño y corte perro pequeño - $35,000")
□ Si tienes promociones activas, cuéntame cuáles

🌐 REDES Y CONTACTO
□ Instagram (si tienes)
□ Facebook (si tienes)
□ ¿Tienes dominio propio? (ej: migroomer.com) Si no, usamos el nuestro gratis.

¿Tienes todo eso? ¡Mándalo y en 48 horas tienes tu página!
```

## Internal checklist (our side)

### On payment received:
- [ ] Create Supabase project for client
- [ ] Copy chosen template to `clients/[client-slug]/`
- [ ] Update .env with new Supabase credentials
- [ ] Create their Hachi account at app.hachi.pet/registro/negocio
- [ ] Get their Hachi slug
- [ ] Run new-client.sh

### On content received:
- [ ] Upload logo to Supabase Storage
- [ ] Upload hero photo
- [ ] Add all services with prices
- [ ] Add team members (if provided)
- [ ] Add gallery photos
- [ ] Configure WhatsApp number
- [ ] Embed Google Maps link
- [ ] Set Hachi slug in admin panel → "Agendar cita" button auto-configures
- [ ] Configure subdomain: [client-slug].studio.hachi.pet
- [ ] If custom domain: update Cloudflare DNS

### On delivery:
- [ ] Test on mobile
- [ ] Send live URL to client
- [ ] Send admin panel login credentials
- [ ] Send 2-min Loom video showing how to update content themselves
- [ ] Add to tracking table in docs/gtm.md
- [ ] Ask for referral (see gtm.md)

## Admin panel login handoff message

```
[Nombre], tu página está viva 🐾🎉

👉 Tu página: [URL]

Para actualizarla tú mismo:
🔧 Panel de administración: [URL]/admin
📧 Usuario: [email]
🔑 Contraseña: [password]

En el panel puedes cambiar:
• Fotos y servicios
• Precios y horarios
• Promociones activas
• Todo desde tu celular

Te mandé un video corto mostrándote cómo funciona 👆

Cualquier duda me escribes aquí. ¡Mucho éxito! 🚀
```

## Hachi onboarding note

After creating their Hachi account:
- Business URL: https://app.hachi.pet/negocio/[slug]
- Booking URL: https://app.hachi.pet/agendamiento/[slug]/servicios
- Send them a separate message explaining Hachi and how to manage bookings
- Reference: ~/zeal/hachi/code/src/lib/helpArticles.ts for Hachi help content
