<template>
  <div>
    <button type="button" :class="className">
      <Icon :name="props.icon" class="text-xl" /> {{ props.text }}
    </button>
  </div>
</template>

<script setup>
const props = defineProps({
  text: { type: String, required: true },
  type: { type: String, required: true },
  icon: { type: String, required: true },
  isBlock: { type: Boolean },
});

let className;

switch (props.type) {
  case "slate":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-slate-600";
    break;
  case "blue":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-blue-800";
    break;
  case "lightgreen":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-[#16a34a]";
    break;
  case "pink":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-rose-500";
    break;
  case "black":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-slate-950";
    break;
  case "green":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-green-700";
    break;
  case "purple":
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-purple-800";
    break;
  default:
    className =
      "text-gray-90 flex gap-2 focus:outline-none focus:ring-4 font-medium rounded-lg text-sm px-3 py-1  me-2 mb-2 text-white bg-green-800";
    break;
}

className += props.isBlock ? " w-full" : "";
</script>
