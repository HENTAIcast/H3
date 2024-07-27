// block for pretty-printing width-constrained strings
    match term_size::dimensions() {
        Some((w, _)) => {
    match terminal_size() {
        Some((Width(width), _)) => {
            let w = width as usize;
            // construct a nice header banner for the update
            let boxie = "#".repeat(w);
            let header = if update.alias.len() > (w - 6) {

.
--------------------
