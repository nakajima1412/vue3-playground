<script setup lang="ts">
import Mention from '@tiptap/extension-mention';
import StarterKit from '@tiptap/starter-kit';
import { useEditor, EditorContent } from '@tiptap/vue-3';

const editor = useEditor({
  content: '',
  editorProps: {
    attributes: {
      class:
        'prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto focus:outline-none',
    },
  },
  extensions: [
    StarterKit,
    // Mention.configure({
    //   HTMLAttributes: {
    //     class: 'mention',
    //   },
    // }),
  ],
});
</script>

<template>
  <EditorContent :editor="editor"></EditorContent>
</template>
