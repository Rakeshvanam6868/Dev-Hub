# 📋 Modern Mobile Dev Stack Checklist

> **The Rule:** Don't build what's already solved. Build what makes your product different.

Use this checklist when starting a new mobile app. For each category, decide:  
✅ **USE** an existing solution — it's a commodity, not your differentiator  
🛠 **BUILD** it yourself — it's your core value, your moat

---

## 🏗 Foundation — USE These

These are solved problems. Don't waste months rebuilding them.

### Cross-Platform Framework
| Option | Why |
|--------|-----|
| **React Native + Expo** | One codebase, iOS + Android. OTA updates. Massive ecosystem. |
| **Flutter** | Great performance, beautiful UI. Smaller ecosystem than RN. |

> 💡 **My pick:** React Native with Expo — used it for [Pulsezy](https://pulsezy.com). Expo's managed workflow saves hundreds of hours.

---

### Backend & Database
| Option | Why |
|--------|-----|
| **Supabase** | Postgres + Auth + Realtime + Storage + Edge Functions. Open source. |
| **Firebase** | Google-backed. Great for prototyping. Vendor lock-in risk. |
| **Appwrite** | Self-hosted alternative. Growing fast. |

> 💡 **My pick:** Supabase — real Postgres, Row Level Security, and Edge Functions. No vendor lock-in.

---

### Authentication
| Option | Why |
|--------|-----|
| **Supabase Auth** | Comes bundled. Email, OAuth, Magic Link, Phone. |
| **Clerk** | Beautiful pre-built UI. Great DX. |
| **Auth0** | Enterprise-grade. More complex setup. |

> 💡 **My pick:** Supabase Auth — zero extra cost, works seamlessly with your database RLS policies.

---

### Navigation
| Option | Why |
|--------|-----|
| **Expo Router** | File-based routing (like Next.js for mobile). Deep linking built-in. |
| **React Navigation** | Battle-tested. More manual setup. |

> 💡 **My pick:** Expo Router — file-based routing is the future of mobile navigation.

---

## 💰 Monetization — USE These

Billing logic is a legal and financial minefield. Don't build it.

### Subscriptions & In-App Purchases
| Option | Why |
|--------|-----|
| **RevenueCat** | Handles Apple + Google receipts, entitlements, analytics. One SDK. |
| **Adapty** | Similar to RevenueCat. Good paywall builder. |
| **Qonversion** | Newer. Solid A/B testing for paywalls. |

> 💡 **My pick:** RevenueCat — handles receipt validation, entitlement management, and analytics. Saved me weeks on Pulsezy.

### Payments (if selling outside app stores)
| Option | Why |
|--------|-----|
| **Stripe** | Industry standard. Great API. |
| **Lemonsqueezy** | Merchant of record. Handles tax globally. |

---

## 📊 Observability — USE These

You can't improve what you can't measure. And you can't fix what you can't see.

### Error Tracking
| Option | Why |
|--------|-----|
| **Sentry** | Real-time crash reports, stack traces, breadcrumbs. |
| **Bugsnag** | Similar. Good mobile-specific features. |

> 💡 **My pick:** Sentry — catches crashes before users report them. Non-negotiable for production apps.

### Analytics
| Option | Why |
|--------|-----|
| **PostHog** | Product analytics + session replay + feature flags. Open source. |
| **Mixpanel** | Event-based analytics. Great funnels. |
| **Amplitude** | Strong for product teams. |

> 💡 **My pick:** PostHog — open source, self-hostable, and does analytics + feature flags + session replay in one tool.

### Performance Monitoring
| Option | Why |
|--------|-----|
| **Sentry Performance** | APM built into your error tracking. |
| **Firebase Performance** | Good baseline monitoring. |

---

## 🎨 UI & Design System — MIX of Build + Use

### Component Libraries
| Option | Why |
|--------|-----|
| **React Native Paper** | Material Design components. Production-ready. |
| **NativeBase** | Accessible, themeable. |
| **Tamagui** | Universal (web + native). Great performance. |
| **Gluestack UI** | Modern, performant, accessible components. |

> 💡 Use a component library as your **base**, but **build custom** for your core product screens.

### Icons
| Option | Why |
|--------|-----|
| **Lucide React Native** | Clean, consistent icon set. |
| **Expo Vector Icons** | Bundled with Expo. Multiple icon sets. |

### Animations
| Option | Why |
|--------|-----|
| **Reanimated** | 60fps native animations. Complex gestures. |
| **Moti** | Simpler API on top of Reanimated. |
| **Lottie** | After Effects animations in your app. |

---

## 🤖 AI & Smart Features — BUILD + USE

### AI API Providers
| Option | Why |
|--------|-----|
| **OpenAI (GPT-4o)** | Best general-purpose. Multimodal. |
| **Anthropic (Claude)** | Great reasoning. Long context. |
| **Google (Gemini)** | Multimodal. Good pricing. |

> 💡 **USE** the API — but **BUILD** the prompt engineering, context management, and user experience around it. That's your moat.

### AI Image/Vision
| Option | Why |
|--------|-----|
| **GPT-4o Vision** | Analyze images (food scanning, form checks, etc.) |
| **Google Cloud Vision** | OCR, label detection. |

---

## 🔔 Push Notifications — USE These

| Option | Why |
|--------|-----|
| **Expo Notifications** | Built into Expo. Easy setup. |
| **OneSignal** | Advanced segmentation, A/B testing. |
| **Firebase Cloud Messaging** | Google's solution. Free. |

> 💡 **My pick:** Expo Notifications for simplicity. OneSignal if you need advanced segmentation.

---

## 🧪 Testing & CI/CD — USE These

### Build & Deploy
| Option | Why |
|--------|-----|
| **EAS Build + Submit** | Expo's cloud build. Submits to stores. |
| **Fastlane** | Open source. More control, more setup. |
| **Codemagic** | CI/CD built for mobile. |

### OTA Updates
| Option | Why |
|--------|-----|
| **EAS Update** | Push JS updates without app store review. |
| **CodePush** | Microsoft's solution. Being deprecated. |

> 💡 **My pick:** EAS Build + EAS Update — build in the cloud, ship updates instantly.

---

## 🗄 Storage & Media — USE These

| Option | Why |
|--------|-----|
| **Supabase Storage** | S3-compatible. Works with your backend. |
| **Cloudinary** | Image/video transformations. CDN. |
| **AWS S3** | Industry standard. More setup. |

---

## 🔐 What You Should BUILD Yourself

This is where your product lives or dies. **Spend your engineering time here.**

| Category | Why Build It |
|----------|-------------|
| **Core Product Logic** | This IS your product. It's what users pay for. |
| **Domain-Specific Algorithms** | Your secret sauce. (e.g., Pulsezy's adaptive training system) |
| **Custom AI Pipelines** | Prompt chains, context management, personalization. |
| **Unique UX Flows** | The experience that makes users say "wow." |
| **Data Models** | Your schema reflects your domain expertise. |
| **Business Rules** | Pricing logic, access control, feature gating. |

---

## ⚡ Quick Decision Framework

Ask yourself for **every feature**:

```
┌─────────────────────────────────────────┐
│  Is this what makes my product unique?  │
├─────────┬───────────────────────────────┤
│   YES   │   NO                          │
├─────────┼───────────────────────────────┤
│ BUILD   │ USE an existing solution      │
│ IT      │ (SDK, API, SaaS)              │
└─────────┴───────────────────────────────┘
```

### The 3 Questions:
1. **Would a user switch to my app because of this feature?** → BUILD it
2. **Does every app need this?** (auth, payments, analytics) → USE it
3. **Am I solving a problem that's already been solved well?** → USE it

---

## 🏆 Real Example: Pulsezy Stack

Here's exactly what I used vs. built for [Pulsezy](https://pulsezy.com):

| Layer | Solution | Build or Use? |
|-------|----------|---------------|
| Framework | React Native + Expo | ✅ USE |
| Backend | Supabase | ✅ USE |
| Auth | Supabase Auth | ✅ USE |
| Database | PostgreSQL (via Supabase) | ✅ USE |
| Subscriptions | RevenueCat | ✅ USE |
| Error Tracking | Sentry | ✅ USE |
| Analytics | PostHog | ✅ USE |
| Push Notifications | Expo Notifications | ✅ USE |
| Builds & Deploys | EAS Build + Update | ✅ USE |
| **Adaptive Training Engine** | Custom algorithm | 🛠 **BUILD** |
| **AI Coaching (Ask Coach)** | Custom pipeline on GPT-4o | 🛠 **BUILD** |
| **Nutrition Scanner** | Custom UX + GPT-4o Vision | 🛠 **BUILD** |
| **Workout Flow UX** | Custom screens & interactions | 🛠 **BUILD** |

> **Result:** 80% of the stack is "used" — freeing up all engineering focus on the 20% that makes Pulsezy *Pulsezy*.

---

## 📌 Save This Checklist

⭐ **Star this repo** to come back to it.  
📤 **Share it** with a dev friend who's starting a new project.  
💬 **DM me on Instagram** [@rakeshvanam](https://instagram.com/rakeshvanam) if you have questions.

---

*Built with real experience, not theory. This is the exact approach I used to ship [Pulsezy](https://pulsezy.com) to production.*

**Build what's unique. Use what's already solved.** 🚀
