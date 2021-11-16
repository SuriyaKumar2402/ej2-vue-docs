---
title: "Comments"
component: "DocumentEditor"
description: "Learn how to perform comments in Vue document editor"
---

# Comments

Document Editor allows you to add comments to documents. You can add, navigate and remove comments in code and from the UI.

## Add a new comment

Comments can be inserted to the selected text.

```typescript
this.$refs.documenteditor.ej2Instances.editor.insertComment("Test comment");
```

## Comment navigation

Next and previous comments can be navigated using the below code snippet.

```typescript
//Navigate to next comment
this.$refs.documenteditor.ej2Instances.selection.navigateNextComment();

//Navigate to previous comment
this.$refs.documenteditor.ej2Instances.selection.navigatePreviousComment();
```

## Delete comment

Current comment can be be deleted using the below code snippet.

```typescript
this.$refs.documenteditor.ej2Instances.editor.deleteComment();
```

## Delete all comment

All the comments in the document can be deleted using the below code snippet.

```typescript
this.$refs.documenteditor.ej2Instances.editor.deleteAllComments();
```
