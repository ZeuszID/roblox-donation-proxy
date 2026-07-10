    local data = HttpService:JSONDecode(message.Data)
    
    print("Platform:", data.platform)    -- saweria/sociabuzz/bagibagi
    print("Donator:", data.donatorName)
    print("Amount:", data.amount)
    print("Message:", data.message)
    
    -- Process donation...
end)
```

## 📦 Data Format

```json
{
    "platform": "saweria|sociabuzz|bagibagi",
    "donatorName": "Nama Donatur",
    "amount": 50000,
    "message": "Pesan donasi",
    "timestamp": 1706612400000
}
```

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Run locally
npm start

# Server akan berjalan di http://localhost:3000
```

## 📝 Files

```
backend/
├── server.js      # Main server (multi-platform + MessagingService)
├── package.json
└── README.md

ServerScriptService/BagiBagi/
└── DonationHandler.lua  # Roblox script dengan MessagingService
```

---

**Versi sebelumnya** menggunakan polling (Roblox request ke server setiap X detik).
**Versi baru** menggunakan push notification (Server kirim langsung ke Roblox saat ada donasi).
