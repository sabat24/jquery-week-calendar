# Requirements

Week calendar relies on jQuery 2.2.0 and jQuery-ui 1.11.2

# Documentation
[Wiki](https://github.com/sabat24/jquery-week-calendar/wiki)

# New Features!

28.02.2019

  - Added breakpoints option to manage options depending on the width of the screen.
  - Added mode *auto* to *height* option.

## Breakpoints usage

*responsive* option is an object containing breakpoints and settings objects for it. Enables settings sets at given screen width.

```js
responsive: [
    {
        breakpoint: 767,
        settings: {
            useShortDayNames: true,
            dateFormat: 'M d, Y',
            daysToShow: 3
        }
    }, {
        breakpoint: 360,
        settings: {
            daysToShow: 1
        }
    }
]
```

Above example shows how to use short date format and show only 3 days on screen width between 360px and 767px. On lower resolution there will be only one day shown.

## Height *auto* mode

When you set option *height* to *auto* the height of whole calendar will be calculated based on timeslots using following formulas.
If you set *businessHours.limitDisplay* to *true*
```
_number_of_bussines_hours_ * timeslotsPerHour * timeslotHeight + _header_height_ + _naviagation_height_
```
If you set *businessHours.limitDisplay* to *false* number_of_bussines_hours will be set to 24.

