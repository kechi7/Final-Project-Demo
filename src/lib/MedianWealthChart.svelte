<script>
    import { onMount } from 'svelte';
    import Chart from 'chart.js/auto';

    let canvas;
    let chart;

    onMount(() => {
        chart = new Chart(canvas, {
            type: 'line',
            data: {
                labels: ['1983', '1990', '2000', '2010', '2019'],
                datasets: [
                    {
                        label: 'Black Median Wealth',
                        data: [10, 12, 14, 13, 15],
                        borderColor: 'rgb(255,99,132)',
                        backgroundColor: 'rgba(255,99,132,0.2)',
                        fill: true
                    },
                    {
                        label: 'White Median Wealth',
                        data: [100, 110, 120, 130, 140],
                        borderColor: 'rgb(54,162,235)',
                        backgroundColor: 'rgba(54,162,235,0.2)',
                        fill: true
                    }
                ]
            },
            options: {
                responsive: true,
                plugins: { legend: { position: 'top' } },
                scales: { y: { title: { display: true, text: 'Median Wealth ($1000s)' } } }
            }
        });
    });
</script>

<canvas bind:this={canvas}></canvas>
