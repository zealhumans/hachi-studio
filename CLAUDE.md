# Hachi Studio — Project Instructions

## What this is

Hachi Studio is a productized web service for the Colombian pet economy.
We build and maintain professional websites for pet businesses in Colombia —
vetted in 48 hours, self-managed via admin panel, connected to Hachi for bookings.

Parent company: Zeal Humans LLC
Domain: studio.hachi.pet
Founders: Antoni Bustamante + Christian Calderón

## Niche (strict — do not deviate)

Any business whose revenue comes from serving animals or their owners:
- Clínicas veterinarias (small/medium)
- Peluquerías / groomers caninos y felinos
- Guarderías y hoteles para mascotas
- Entrenadores caninos / academias de adiestramiento
- Tiendas de mascotas specialty
- Pet sitters / cuidadores a domicilio
- Servicios veterinarios a domicilio
- Fotografía de mascotas
- Spas para mascotas
- Fundaciones y centros de rescate

NOT our niche: gyms, salons, restaurants, coaches, fashion — anything not tied to animals.

## Pricing (non-negotiable)

- Setup: $500,000 COP (one-time)
- Mantenimiento: $25,000 COP/mes
- Anual: $800,000 COP/año
- Guarantee: live in 48h or setup refunded

## Tech stack

- Landing page: HTML + Tailwind CDN (static, deployed to Cloudflare Pages)
- Client sites: React 19 + TanStack Start + Supabase + Cloudflare Workers
  (forked from project-companion at ~/Downloads/project-companion-main.zip)
- Per client: separate Supabase project + subdomain [slug].studio.hachi.pet
- Hachi booking button: https://app.hachi.pet/agendamiento/{slug}/servicios

## Hachi integration

Every client gets a free Hachi account during onboarding.
Their "Agendar cita" button links to their Hachi booking flow.
Reference: ~/zeal/hachi/code/src/lib/slugValidation.ts → getBookingUrl()

## Language rules

- All customer-facing copy: Colombian Spanish
- Prices: always COP, never USD
- Code, commits, internal docs: English
- Timezone: America/Bogota

## Folder map

- landing/      → sales page for studio.hachi.pet (the offer site)
- templates/    → 10 client site templates (vitrina, estrella, raices, plaza, esencia, ...)
- scripts/      → new-client.sh (clone → configure → deploy per client)
- clients/      → deployed client instances
- docs/         → offer spec, GTM playbook, onboarding checklist, pricing
