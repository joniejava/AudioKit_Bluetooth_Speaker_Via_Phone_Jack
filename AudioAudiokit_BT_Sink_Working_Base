// ✅ WORKING SETUP — AudioKit v2.2 + Bluetooth A2DP Sink
// Tested: 2025-10-06 on macOS
// Notes: Plays Bluetooth audio from iPhone → 3.5mm jack (ES8388 DAC active)
// Libraries:
//   - audio-tools v1.2.0
//   - ESP32-A2DP v1.8.7
//   - ESP32 board package v2.0.14


#include "AudioTools.h"
#include "AudioTools/AudioLibs/AudioKit.h"
#include "BluetoothA2DPSink.h"

using namespace audio_tools;

AudioKitStream kit;
BluetoothA2DPSink a2dp_sink;

void setup() {
  Serial.begin(115200);
  Serial.println("🎧 Starting Bluetooth A2DP → AudioKit receiver...");

  AudioLogger::instance().begin(Serial, AudioLogger::Warning);

  auto cfg = kit.defaultConfig(TX_MODE);
  cfg.sample_rate     = 44100;
  cfg.bits_per_sample = 16;
  cfg.channels        = 2;
  cfg.sd_active       = false;
  kit.begin(cfg);
  kit.setVolume(80);
  Serial.println("✅ AudioKit initialized (DAC active)");

  // Configure Bluetooth A2DP sink
  a2dp_sink.set_auto_reconnect(true);
  a2dp_sink.set_volume(60);

  i2s_pin_config_t pins = {
      .bck_io_num   = cfg.pin_bck,
      .ws_io_num    = cfg.pin_ws,
      .data_out_num = cfg.pin_data,
      .data_in_num  = I2S_PIN_NO_CHANGE
  };

  a2dp_sink.set_pin_config(pins);
  a2dp_sink.set_i2s_port((i2s_port_t)cfg.port_no);

  // Optional: small delay before starting BT stack
  delay(500);

  Serial.println("📱 Pair your phone to 'AudioKit_ESP32' (A2DP Sink)");
  a2dp_sink.start("AudioKit_ESP32", true);

  // --- Workaround: Restart I2S after BT init ---
  Serial.println("🔄 Reinitializing I2S...");
  kit.end();
  delay(200);
  kit.begin(cfg);

  Serial.println("🎶 Ready — play audio on your phone to test the 3.5mm jack!");
}

void loop() {
  delay(100);
}

