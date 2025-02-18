#!/bin/sh
echo "🔍 Exécution du linter..."
eslint . || exit 1

