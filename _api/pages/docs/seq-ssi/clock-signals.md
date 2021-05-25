{
  "name": "clock-signals.md",
  "path": "docs/seq-ssi/clock-signals.md",
  "relative_path": "docs/seq-ssi/clock-signals.md",
  "layout": "circuitverse",
  "title": "Clock signals",
  "nav_order": "l0s002",
  "cvib_level": "basic",
  "parent": "Sequential SSI",
  "has_children": false,
  "content": "<h1 class=\"no_toc\" id=\"clock-signals\">Clock signals</h1>\n\n<h2 class=\"no_toc text-delta\" id=\"table-of-contents\">Table of contents</h2>\n\n<ol id=\"markdown-toc\">\n  <li><a href=\"#clock-signal\" id=\"markdown-toc-clock-signal\">Clock signal</a></li>\n  <li><a href=\"#types-of-triggering\" id=\"markdown-toc-types-of-triggering\">Types of triggering</a>    <ol>\n      <li><a href=\"#level-triggering\" id=\"markdown-toc-level-triggering\">Level triggering</a></li>\n      <li><a href=\"#edge-triggering\" id=\"markdown-toc-edge-triggering\">Edge triggering</a></li>\n    </ol>\n  </li>\n</ol>\n\n<h2 id=\"clock-signal\">Clock signal</h2>\n\n<p>Clock signal is a periodic signal and its ON time and OFF time need not be the same. \nYou can represent the clock signal as a square wave, when both its ON time and OFF time are same. \nThis clock signal is shown in the following figure.</p>\n\n<div style=\"text-align:center\"><img src=\"/assets/images/clock_signal.jpg\" /></div>\n\n<p>In the above figure, square wave is considered as clock signal. This signal stays at logic High (5V) for some time and stays at logic Low (0V) for equal amount of time. This pattern repeats with some time period. In this case, the time period will be equal to either twice of ON time or twice of OFF time.</p>\n\n<p>You can represent the clock signal as train of pulses, when ON time and OFF time are not same. This clock signal is shown in the following figure.</p>\n\n<div style=\"text-align:center\"><img src=\"/assets/images/train_of_pulses.jpg\" /></div>\n\n<p>In the above figure, train of pulses is considered as clock signal. This signal stays at logic High (5V) for some time and stays at logic Low (0V) for some other time. This pattern repeats with some time period. In this case, the time period will be equal to sum of ON time and OFF time.</p>\n\n<p>The reciprocal of the time period of clock signal is known as the frequency of the clock signal. All sequential circuits are operated with clock signal. So, the frequency at which the sequential circuits can be operated accordingly the clock signal frequency has to be chosen.</p>\n\n<h2 id=\"types-of-triggering\">Types of triggering</h2>\n\n<p>Following are the two possible types of triggering that are used in sequential circuits.</p>\n\n<ul>\n  <li>Level triggering</li>\n  <li>Edge triggering</li>\n</ul>\n\n<h3 id=\"level-triggering\">Level triggering</h3>\n\n<p>There are two levels, namely logic High and logic Low in clock signal. Following are the two types of <strong>level triggering</strong>.</p>\n\n<ul>\n  <li>Positive level triggering</li>\n  <li>Negative level triggering</li>\n</ul>\n\n<p>If the sequential circuit is operated with the clock signal when it is in <strong>Logic High</strong>, then that type of triggering is known as <strong>Positive level triggering</strong>. It is highlighted in below figure.</p>\n<div style=\"text-align:center\"><img src=\"/assets/images/level_triggering.jpg\" /></div>\n\n<p>If the sequential circuit is operated with the clock signal when it is in <strong>Logic Low</strong>, then that type of triggering is known as <strong>Negative level triggering</strong>. It is highlighted in the following figure.</p>\n\n<div style=\"text-align:center\"><img src=\"/assets/images/negative_level_triggering.jpg\" /></div>\n\n<h3 id=\"edge-triggering\">Edge triggering</h3>\n\n<p>There are two types of transitions that occur in clock signal. That means, the clock signal transitions either from Logic Low to Logic High or Logic High to Logic Low.</p>\n\n<p>Following are the two types of edge triggering based on the transitions of clock signal.</p>\n\n<ul>\n  <li>Positive edge triggering</li>\n  <li>Negative edge triggering</li>\n</ul>\n\n<p>If the sequential circuit is operated with the clock signal that is transitioning from Logic Low to Logic High, then that type of triggering is known as <strong>Positive edge triggering</strong>. It is also called as <strong>rising edge triggering</strong>. It is shown in the following figure.</p>\n\n<div style=\"text-align:center\"><img src=\"/assets/images/positive_edge_triggering.jpg\" /></div>\n\n<p>If the sequential circuit is operated with the clock signal that is transitioning from Logic High to Logic Low, then that type of triggering is known as <strong>Negative edge triggering</strong>. It is also called as <strong>falling edge triggering</strong>. It is shown in the following figure.</p>\n\n<div style=\"text-align:center\"><img src=\"/assets/images/negative_edge_triggering.jpg\" /></div>\n",
  "dir": "/docs/seq-ssi/",
  "url": "/docs/seq-ssi/clock-signals.html",
  "raw_content": "# Clock signals\n{: .no_toc}\n\n\n## Table of contents\n{: .no_toc .text-delta}\n\n1. TOC\n{:toc}\n\n## Clock signal\n\nClock signal is a periodic signal and its ON time and OFF time need not be the same. \nYou can represent the clock signal as a square wave, when both its ON time and OFF time are same. \nThis clock signal is shown in the following figure.\n\n<div style=\"text-align:center\"><img src=\"/assets/images/clock_signal.jpg\" /></div>\n\nIn the above figure, square wave is considered as clock signal. This signal stays at logic High (5V) for some time and stays at logic Low (0V) for equal amount of time. This pattern repeats with some time period. In this case, the time period will be equal to either twice of ON time or twice of OFF time.\n\nYou can represent the clock signal as train of pulses, when ON time and OFF time are not same. This clock signal is shown in the following figure.\n\n<div style=\"text-align:center\"><img src=\"/assets/images/train_of_pulses.jpg\" /></div>\n\nIn the above figure, train of pulses is considered as clock signal. This signal stays at logic High (5V) for some time and stays at logic Low (0V) for some other time. This pattern repeats with some time period. In this case, the time period will be equal to sum of ON time and OFF time.\n\nThe reciprocal of the time period of clock signal is known as the frequency of the clock signal. All sequential circuits are operated with clock signal. So, the frequency at which the sequential circuits can be operated accordingly the clock signal frequency has to be chosen.\n\n## Types of triggering\n\nFollowing are the two possible types of triggering that are used in sequential circuits.\n\n- Level triggering\n- Edge triggering\n\n### Level triggering\n\nThere are two levels, namely logic High and logic Low in clock signal. Following are the two types of **level triggering**.\n\n- Positive level triggering\n- Negative level triggering\n\nIf the sequential circuit is operated with the clock signal when it is in **Logic High**, then that type of triggering is known as **Positive level triggering**. It is highlighted in below figure.\n<div style=\"text-align:center\"><img src=\"/assets/images/level_triggering.jpg\" /></div>\n\nIf the sequential circuit is operated with the clock signal when it is in **Logic Low**, then that type of triggering is known as **Negative level triggering**. It is highlighted in the following figure.\n\n<div style=\"text-align:center\"><img src=\"/assets/images/negative_level_triggering.jpg\" /></div>\n\n### Edge triggering\n\nThere are two types of transitions that occur in clock signal. That means, the clock signal transitions either from Logic Low to Logic High or Logic High to Logic Low.\n\nFollowing are the two types of edge triggering based on the transitions of clock signal.\n\n- Positive edge triggering\n- Negative edge triggering\n\nIf the sequential circuit is operated with the clock signal that is transitioning from Logic Low to Logic High, then that type of triggering is known as **Positive edge triggering**. It is also called as **rising edge triggering**. It is shown in the following figure.\n\n<div style=\"text-align:center\"><img src=\"/assets/images/positive_edge_triggering.jpg\" /></div>\n\nIf the sequential circuit is operated with the clock signal that is transitioning from Logic High to Logic Low, then that type of triggering is known as **Negative edge triggering**. It is also called as **falling edge triggering**. It is shown in the following figure.\n\n<div style=\"text-align:center\"><img src=\"/assets/images/negative_edge_triggering.jpg\" /></div>\n",
  "front_matter": {
    "layout": "circuitverse",
    "title": "Clock signals",
    "nav_order": "l0s002",
    "cvib_level": "basic",
    "parent": "Sequential SSI",
    "has_children": false
  },
  "front_matter_defaults": {
  },
  "http_url": "https://manjotsidhu.github.io/Interactive-Book/docs/seq-ssi/clock-signals.html",
  "api_url": "https://manjotsidhu.github.io/Interactive-Book/_api/pages/docs/seq-ssi/clock-signals.md"
}