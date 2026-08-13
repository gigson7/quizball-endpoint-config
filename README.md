# QuizBall endpoint configuration

This public repository serves QuizBall's Ed25519-signed endpoint configuration
through GitHub Pages. The app verifies the signature before using the document.

Only a previously signed `v1/config.json` may be published. The signing private
key must never be committed, uploaded to GitHub, placed in Actions secrets, or
copied to the application server. Supabase publishable/anon keys are client
credentials and may appear in the signed payload; secret/service-role keys are
forbidden.

The canonical signer and verification tooling live in the private QuizBall
application repository under `deploy/endpoint-config/`.
