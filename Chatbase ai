<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chatbot</title>
</head>
<body>
    <h2>Chat with AI</h2>
    
    <!-- Chatbase Script -->
    <script>
        (function(){
            if(!window.chatbase || window.chatbase("getState") !== "initialized") {
                window.chatbase = (...arguments) => {
                    if (!window.chatbase.q) { window.chatbase.q = []; }
                    window.chatbase.q.push(arguments);
                };
                window.chatbase = new Proxy(window.chatbase, {
                    get(target, prop) {
                        if (prop === "q") { return target.q; }
                        return (...args) => target(prop, ...args);
                    }
                });
            }
            const onLoad = function() {
                const script = document.createElement("script");
                script.src = "https://www.chatbase.co/embed.min.js";
                script.id = "chatbase-script"; // Give an ID to track
                script.domain = "www.chatbase.co";
                document.body.appendChild(script);
            };
            if (document.readyState === "complete") {
                onLoad();
            } else {
                window.addEventListener("load", onLoad);
            }
        })();
    </script>
</body>
</html>
