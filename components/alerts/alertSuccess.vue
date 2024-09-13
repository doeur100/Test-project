<template>
    <button @click="clickAlert()">Click</button>
</template>

<script setup>
    import Swal from "sweetalert2";
    const clickAlert = () => {
    Swal.fire({
    position: "top-end",
    icon: "success",
    title: "Your work has been saved",
    showConfirmButton: false,
    timer: 1500
});
};
</script>