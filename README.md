# Subtitle System — UE5.3

Localised subtitle system built for *57Knives*, in development at Frisant Games. Shipped with Catalan, Spanish and English; adding a language is a row in a data table, not a code change.

**Source is not public.** The project is under NDA, so this repository holds the screenshots and the write-up rather than the code. Happy to walk through the implementation in a call.

## How it works

Subtitle lines live in a data table keyed by line ID, with one column per language. The widget reads the active language from the player's settings and pulls the matching column, so the whole system has a single point of change when a new language arrives: add the column, fill the rows, add the entry to the language menu.

Timing and display are driven from the audio events rather than from a separate timeline, which keeps subtitles in sync when dialogue is interrupted or skipped.

## Language selection

![Language menu](https://github.com/user-attachments/assets/14ff1bf5-c727-43dc-a7f8-9c554d347d2b)

## The same line in Catalan, Spanish and English

![Catalan](https://github.com/user-attachments/assets/a20a2f6b-6ccb-4e9d-a945-9be3e54c0f4b)
![Spanish](https://github.com/user-attachments/assets/f069ac04-39d8-48ec-a978-1c2342c0f708)
![English](https://github.com/user-attachments/assets/8d54ee7c-0159-4715-b7e8-c6eb1659cd73)

## Adding a language

![Data table](https://github.com/user-attachments/assets/5b2659e0-2f6c-478f-b9c3-23e54d218fdf)
