---
type: dashboard
---

# 🏛️ Omni_OS — Strategic Dashboard

---

## 📊 Annual Weekly Heatmap (2026)

> Monitoramento visual das semanas concluídas e hábitos consolidados do seu Second Brain:

```dataviewjs
// Certifique-se de ter o plugin "Heatmap Tracker" ativado nas configurações
const calendarData = {
    year: 2026,
    colors: {
        blue: ["#8fa3bf", "#5b7cb8", "#2f59a8", "#123780", "#082154"]
    },
    entries: []
}

// O script agora varre a sua nova pasta de notas semanais
for (let page of dv.pages('"00_Sessao_Tecnica/weekly_records"')) {
    // Alimenta o gráfico se você marcou que estudou na UFMT naquela semana
    if (page.ufmt_study === true) {
        calendarData.entries.push({
            date: page.date, // Puxa a data do domingo de criação
            intensity: 4,
            content: "🏫"
        })
    }
}

renderHeatmapCalendar(this.container, calendarData)
```

---

## 🗓️ Today's Action Items (Ações de Hoje)

```tasks
not done
# Mostra todas as tarefas pendentes da sua nota semanal ativa
path includes 00_Sessao_Tecnica/weekly_records
short mode
```

---

## 📅 Next 7 Days (Weekly Outlook)

```tasks
not done
# Mostra o planejamento geral que está dentro do seu semanário estruturado
path includes 00_Sessao_Tecnica/weekly_records
heading includes Tasks da Semana
```

---

## 🏆 Recently Completed (Concluído Recentemente)

```tasks
done
# Lista tudo o que você deu check nos últimos 7 dias para dar satisfação mental
done after 7 days ago
```