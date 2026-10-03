---
type: dashboard
tags:
  - dashboard
  - overview
  - omni_os
---

# 🏛️ Omni_OS — Strategic Dashboard

---

## 📊 Annual Habit Heatmap

> Visualização automatizada do seu progresso em estudo de dev em 2026:

```dataviewjs
const calendarData = {
    year: 2026,
    colors: {
        blue: ["#8fa3bf", "#5b7cb8", "#2f59a8", "#123780", "#082154"]
    },
    entries: []
}

for (let page of dv.pages('"00_Sessao_Tecnica/Daily_Notes"')) {
    if (page.dev_html === true) {
        calendarData.entries.push({
            date: page.date,
            intensity: 4,
            content: "💻"
        })
    }
}

renderHeatmapCalendar(this.container, calendarData)
```

---

## 🗓️ Today's Action Items

```tasks
not done
due before or on today
sort by priority
```

---

## 📅 Next 7 Days (Weekly Outlook)

```tasks
not done
due after today
due before in 7 days
```

---

## 🏆 Recently Completed

```tasks
done
done after 7 days ago
```