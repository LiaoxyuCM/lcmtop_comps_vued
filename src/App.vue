<script setup>
import Navbar from "./components/Navbar.vue";
import Card from "./components/Card.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
    <Navbar />
    <div class="mainpare">
        <main>
            <div class="cards">
                <Card
                    title="Hi"
                    content="self"
                    link="https://example.com"
                    :visible="true"
                />
            </div>
        </main>
    </div>
    <Footer />
</template>
