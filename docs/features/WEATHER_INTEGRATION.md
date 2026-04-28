# Weather Integration

This manual explains weather information available in Contact Ground. Weather data is retrieved from [aviationweather.gov](aviationweather.gov) and may not always be available for airports outside of the US.

## 1. What Weather Integration Provides

The app surfaces aviation weather context for planning and operational awareness, including:
1. METAR conditions at your organization's home base
2. TAF forecast context
3. Weather widgets on the dashboard

## 2. Home Base Requirement

Weather is tied to your organization's configured home base. To configure your home base, go to the `Organization` page and enter the ICAO identifier for your primary airport.

## 3. Reading the Weather Widget

The weather widget appears on the dashboard and surfaces current and forecast conditions for your organization's home base.

### 3.1 METAR (Current Conditions)

The METAR section displays the most recent automated weather observation from your home base:

- **Raw METAR text**: The complete observation in standard aviation format (for example, `METAR KPHL 191255Z 27008KT 10SM FEW030 BKN070 12/04 A2998`).
- **Color coding**: The text color reflects the overall weather condition:
  - Green: Visual Meteorological Conditions (VMC)—generally flyable VFR conditions
  - Blue: Instrument Meteorological Conditions (IMC) or lower
  - Red/amber: Significant weather restrictions present
- **Weather icon**: A visual indicator of general conditions (clear, clouds, rain, etc.)
- **Status message**: If weather data is temporarily unavailable, a status message is displayed instead of the observation.

METAR data is refreshed automatically at regular intervals.

### 3.2 TAF (Terminal Aerodrome Forecast)

The TAF section shows the current forecast for your home base or the nearest station with an available forecast:

- **Forecast sections**: The full TAF is broken into time periods. Each period shows the forecast conditions for that time window.
- **Current period**: The period currently in effect is highlighted with a 👉 indicator.
- **Color coding**: Each period is color-coded using the same scheme as METAR (green/blue/red).
- **Alternate station note**: If the TAF is from a different station than the home base METAR, the widget shows the alternate station identifier and its distance from your home base (for example, `TAF from KJFK (25 nm from KPHL)`).

TAF data is refreshed automatically at regular intervals.

### 3.3 What to do when weather data is unavailable

If the widget shows a status message rather than weather data:
1. Wait a few minutes and reload the page. Data is fetched from an external source and may occasionally be delayed.
2. Check that your home base ICAO identifier is correctly configured in `Organization` settings.
3. If the issue persists, contact your organization admin.

## 4. How Members Use Weather Data

1. Review the weather widget before scheduling a flight. Current conditions and the forecast provide helpful context for planning.
2. Use the METAR to assess conditions at the field right now.
3. Use the TAF to understand what conditions are forecast during your planned flight window.
4. Watch for weather-related notifications when enabled in your notification preferences.

## 5. How Weather Affects Flight Planning

The weather widget is a planning aid. Use it to inform decisions about whether and when to fly. Consider:

- **VFR vs. IFR**: Green-coded conditions suggest VFR is likely available. Blue or red coding indicates conditions may require an instrument approach or may not be suitable for VFR flight.
- **Trend awareness**: Review multiple TAF periods to understand whether conditions are improving or deteriorating.
- **Time of flight**: Identify which TAF period covers your planned departure and return time and review the forecast conditions for that window.

Weather does not automatically block or modify bookings. It is your responsibility to assess conditions and determine whether a flight is appropriate. If your organization has enabled weather-related notifications, you may receive alerts when significant weather changes are detected near your scheduled flight time—see your `Profile` → `Notification Preferences` to manage this setting.

## 6. What Weather Data Is For

Weather integration supports decision-making. It does not replace pilot judgment, official briefings, or required preflight planning processes.

## 7. Best Practices

1. Treat in-app weather as a planning aid.
2. Always complete your standard weather briefing workflow before flight.
3. Monitor weather changes as departure time approaches.
4. Use the color coding as a quick reference, not as a go/no-go determination.
5. Ensure your organization's home base ICAO is correctly configured for accurate weather display.
