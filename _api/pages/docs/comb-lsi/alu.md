{
  "name": "alu.md",
  "path": "docs/comb-lsi/alu.md",
  "relative_path": "docs/comb-lsi/alu.md",
  "layout": "circuitverse",
  "title": "ALU",
  "nav_order": "l0s001",
  "cvib_level": "basic",
  "parent": "Combinational LSI",
  "has_children": false,
  "content": "<h1 class=\"no_toc\" id=\"arithmetic-logic-unit\">Arithmetic Logic Unit</h1>\n\n<h2 class=\"no_toc text-delta\" id=\"table-of-contents\">Table of contents</h2>\n\n<ol id=\"markdown-toc\">\n  <li><a href=\"#introduction\" id=\"markdown-toc-introduction\">Introduction</a></li>\n  <li><a href=\"#in-detail\" id=\"markdown-toc-in-detail\">In detail</a></li>\n</ol>\n\n<h2 id=\"introduction\">Introduction</h2>\n<p>An arithmetic logic unit (ALU) is a digital circuit used to perform arithmetic and logic operations. It represents the fundamental building block of the central processing unit (CPU) of a computer. Modern CPUs contain very powerful and complex ALUs. In addition to ALUs, modern CPUs contain a control unit (CU).</p>\n\n<p>The purpose of the ALU is to perform mathematical operations such as addition, subtraction, multiplication and division. Additionally, the ALU processes basic logical operations like AND/OR calculations. It serves as the computational hub of the Central Processing Unit (CPU) for a computer system</p>\n\n<h2 id=\"in-detail\">In detail</h2>\n<p>So with the above building blocks i.e. half adder and full adder discussed in Combinational Analysis, lets construct a simple ALU that performs a arithmetic operation (1 bit addition) and does 3 logical operations namely AND, NOR and XOR as shown below. The multiplexer selects only one operation at a time. The operation selected depends on the selection lines of the multiplexer as shown in the truth table.</p>\n\n<iframe width=\"100%\" height=\"400px\" src=\"https://circuitverse.org/simulator/embed/42961\" id=\"alu_01\" scrolling=\"no\" webkitallowfullscreen=\"\" mozallowfullscreen=\"\" allowfullscreen=\"\"> </iframe>\n\n<p><strong>Input = M0,M1 &amp; \nOutput = Operation</strong></p>\n\n<table>\n  <thead>\n    <tr>\n      <th style=\"text-align: center\">M0</th>\n      <th style=\"text-align: center\">M1</th>\n      <th style=\"text-align: center\">Operation</th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <td style=\"text-align: center\">0</td>\n      <td style=\"text-align: center\">0</td>\n      <td style=\"text-align: center\">SUM</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">0</td>\n      <td style=\"text-align: center\">1</td>\n      <td style=\"text-align: center\">AND</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">1</td>\n      <td style=\"text-align: center\">0</td>\n      <td style=\"text-align: center\">OR</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">1</td>\n      <td style=\"text-align: center\">1</td>\n      <td style=\"text-align: center\">XOR</td>\n    </tr>\n  </tbody>\n</table>\n\n<p>Now you can take up the 1 bit ALU as block and construct a 4 bit ALU, which performs all the functions of the 1 bit ALU on the 4 bit inputs. Thus a single building block can be constructed and used recursively. The inputs A and B are four bits and the output is 4 bit as well. Figure below illustrates it:</p>\n\n<div style=\"text-align:center\"><img src=\"/assets/images/360px-4BITALU.jpg\" /></div>\n\n<p>There are a few important takeaways here:</p>\n<ul>\n  <li>The selection lines MO and M1 select the function ALU performs. These selection lines combined with the input arguments and desired functions, an Instruction Set can be formed.</li>\n  <li>These Instructions can used to create meaningful programs. Since these are required to be easily available, they can be stored on ROM unit.</li>\n  <li>The input arguments A and B are often stored in Internal Registers. These along with other special purpose register form the registers of the microcontroller.</li>\n  <li>ROM memories are slower in speed, hence an intermediate high speed RAM is often used.</li>\n  <li>All the critical timings, decoding of the instructions are often grouped together in seperate control and timings unit.</li>\n  <li>If a Micro controller would be constructed only from ALU, RAM and ROM, there would not be any external interface. Hence, you now have Input/Output (I/O) ports.</li>\n  <li>Additional features such as Interrupts, communication protocols, EEPROM, Timers/Counters, Debug interfaces etc. are incorporated to make a controller complete.</li>\n</ul>\n\n<p>In above discussion you might have left out intricate details involved in an ALU, CPU design. But the aim was to understand ALU/CPU at a deeper level.</p>\n\n<style>\nimg{\n    max-width:50%;\n}\n</style>\n\n",
  "dir": "/docs/comb-lsi/",
  "url": "/docs/comb-lsi/alu.html",
  "raw_content": "# Arithmetic Logic Unit\n{: .no_toc}\n\n\n## Table of contents\n{: .no_toc .text-delta}\n\n1. TOC\n{:toc}\n\n## Introduction\nAn arithmetic logic unit (ALU) is a digital circuit used to perform arithmetic and logic operations. It represents the fundamental building block of the central processing unit (CPU) of a computer. Modern CPUs contain very powerful and complex ALUs. In addition to ALUs, modern CPUs contain a control unit (CU).\n\nThe purpose of the ALU is to perform mathematical operations such as addition, subtraction, multiplication and division. Additionally, the ALU processes basic logical operations like AND/OR calculations. It serves as the computational hub of the Central Processing Unit (CPU) for a computer system\n\n## In detail\nSo with the above building blocks i.e. half adder and full adder discussed in Combinational Analysis, lets construct a simple ALU that performs a arithmetic operation (1 bit addition) and does 3 logical operations namely AND, NOR and XOR as shown below. The multiplexer selects only one operation at a time. The operation selected depends on the selection lines of the multiplexer as shown in the truth table.\n\n<iframe width=\"100%\" height=\"400px\" src=\"https://circuitverse.org/simulator/embed/42961\" id=\"alu_01\" scrolling=\"no\" webkitAllowFullScreen mozAllowFullScreen allowFullScreen> </iframe>\n\n**Input = M0,M1 & \nOutput = Operation**\n\n|M0|M1|Operation|\n|:-:|:-:|:-------:|\n|0\t|0\t|SUM|\n|0\t|1\t|AND|\n|1\t|0\t|OR|\n|1\t|1\t|XOR|\n\n\nNow you can take up the 1 bit ALU as block and construct a 4 bit ALU, which performs all the functions of the 1 bit ALU on the 4 bit inputs. Thus a single building block can be constructed and used recursively. The inputs A and B are four bits and the output is 4 bit as well. Figure below illustrates it:\n\n<div style=\"text-align:center\" ><img src=\"/assets/images/360px-4BITALU.jpg\" /></div>\n\nThere are a few important takeaways here:\n- The selection lines MO and M1 select the function ALU performs. These selection lines combined with the input arguments and desired functions, an Instruction Set can be formed.\n- These Instructions can used to create meaningful programs. Since these are required to be easily available, they can be stored on ROM unit.\n- The input arguments A and B are often stored in Internal Registers. These along with other special purpose register form the registers of the microcontroller.\n- ROM memories are slower in speed, hence an intermediate high speed RAM is often used.\n- All the critical timings, decoding of the instructions are often grouped together in seperate control and timings unit.\n- If a Micro controller would be constructed only from ALU, RAM and ROM, there would not be any external interface. Hence, you now have Input/Output (I/O) ports.\n- Additional features such as Interrupts, communication protocols, EEPROM, Timers/Counters, Debug interfaces etc. are incorporated to make a controller complete.\n\nIn above discussion you might have left out intricate details involved in an ALU, CPU design. But the aim was to understand ALU/CPU at a deeper level.\n\n<style>\nimg{\n    max-width:50%;\n}\n</style>\n",
  "front_matter": {
    "layout": "circuitverse",
    "title": "ALU",
    "nav_order": "l0s001",
    "cvib_level": "basic",
    "parent": "Combinational LSI",
    "has_children": false
  },
  "front_matter_defaults": {
  },
  "http_url": "https://manjotsidhu.github.io/Interactive-Book/docs/comb-lsi/alu.html",
  "api_url": "https://manjotsidhu.github.io/Interactive-Book/_api/pages/docs/comb-lsi/alu.md"
}