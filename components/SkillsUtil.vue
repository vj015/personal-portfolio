<template>
  <div ref="skillsContainer" class="skills"></div>
</template>

<script>
export default {
  name: "SkillsPentagon",
  data() {
    return {
      skills: [
        {
          header: "INTERESTS",
          captions: ["Architecture", "Performance", "PWAs", "Design", "Fintech"],
          values: [0.8, 0.9, 0.7, 0.8, 0.9],
        },
        {
          header: "CORE",
          captions: ["JS", "Java", "HTML", "Reactivity", "Workflow"],
          values: [0.9, 0.7, 0.9, 0.7, 0.8],
        },
        {
          header: "Modern Web",
          captions: ["Vue", "Nuxt", "React", "Spring", "Temporal"],
          values: [0.8, 0.85, 0.9, 0.75, 0.6],
        },
      ],
      hue: [],
      hueOffset: 25,
      pentagonIndex: 0,
      valueIndex: 0,
      width: 0,
      height: 0,
      radOffset: Math.PI / 2,
      sides: 5,
      theta: (2 * Math.PI) / 5,
    };
  },
  methods: {
    getXY(i, radius) {
      return {
        x:
          Math.cos(this.radOffset + this.theta * i) * radius * this.width +
          this.width / 2,
        y:
          Math.sin(this.radOffset + this.theta * i) * radius * this.height +
          this.height / 2,
      };
    },
    drawPentagon() {
      this.skills.forEach((skill, s) => {
        // Ensure the skillsContainer exists
        if (this.$refs.skillsContainer) {
          this.$refs.skillsContainer.insertAdjacentHTML(
            "beforeend",
            '<div class="pentagon"><div class="header"></div><canvas class="pentCanvas"></canvas></div>'
          );
        }
        this.hue[s] = (this.hueOffset + (s * 255) / this.skills.length) % 255;
      });

      this.$refs.skillsContainer
        .querySelectorAll(".pentagon")
        .forEach((element, index) => {
          this.width = element.clientWidth;
          this.height = element.clientHeight;
          const canvas = element.querySelector("canvas");
          const ctx = canvas.getContext("2d");
          canvas.width = this.width;
          canvas.height = this.height;
          ctx.font = "15px Monospace";
          ctx.textAlign = "center";

          /*** LABEL ***/
          const color = `hsl(${this.hue[this.pentagonIndex]}, 100%, 30%)`;
          ctx.fillStyle = color;
          ctx.fillText(
            this.skills[this.pentagonIndex].header,
            this.width / 2,
            15
          );
          ctx.font = "13px Monospace";

          /*** PENTAGON BACKGROUND ***/
          for (let i = 0; i < this.sides; i++) {
            // For each side, draw two segments: the side, and the radius
            ctx.beginPath();
            let xy = this.getXY(i, 0.3);
            const colorJitter = 25 + this.theta * i * 2;
            const sideColor = `hsl(${
              this.hue[this.pentagonIndex]
            }, 100%, ${colorJitter}%)`;
            ctx.fillStyle = sideColor;
            ctx.strokeStyle = sideColor;
            ctx.moveTo(0.5 * this.width, 0.5 * this.height); // center
            ctx.lineTo(xy.x, xy.y);
            xy = this.getXY(i + 1, 0.3);
            ctx.lineTo(xy.x, xy.y);
            xy = this.getXY(i, 0.37);
            ctx.fillText(
              this.skills[this.pentagonIndex].captions[this.valueIndex],
              xy.x,
              xy.y + 5
            );
            this.valueIndex++;
            ctx.closePath();
            ctx.fill();
            ctx.stroke();
          }

          this.valueIndex = 0;
          ctx.beginPath();
          ctx.fillStyle = "rgba(0, 0, 0, 0.2)";
          ctx.strokeStyle = "rgba(0, 0, 0, 0.3)";
          ctx.lineWidth = 5;
          let value = this.skills[this.pentagonIndex].values[this.valueIndex];
          let xy = this.getXY(index, value * 0.3);
          ctx.moveTo(xy.x, xy.y);

          /*** SKILL GRAPH ***/
          for (let i = 0; i < this.sides; i++) {
            xy = this.getXY(i, value * 0.3);
            ctx.lineTo(xy.x, xy.y);
            this.valueIndex++;
            value = this.skills[this.pentagonIndex].values[this.valueIndex];
          }
          ctx.closePath();
          ctx.stroke();
          ctx.fill();
          this.valueIndex = 0;
          this.pentagonIndex++;
        });
    },
  },
  mounted() {
    this.drawPentagon();
  },
};
</script>

<style scoped>
.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}
.pentagon {
  position: relative;
  width: 200px;
  height: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.pentCanvas {
  position: absolute;
  top: 0;
  left: 0;
}
.header {
  margin-bottom: 10px;
  font-weight: bold;
}
</style>
