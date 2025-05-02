 from flask import Flask, request, jsonify

app = Flask(__name__)

@app.route("/api/check_pubg", methods=["POST"])
def check_pubg():
    data = request.json
    username = data.get("username")

    if not username:
        return jsonify({"status": "error", "message": "يرجى إدخال ID أو إيميل"}), 400

    if "123" in username or "@gmail.com" in username:
        return jsonify({"status": "found", "message": "✓ الحساب موجود في ببجي"})
    else:
        return jsonify({"status": "not_found", "message": "✗ الحساب غير موجود"})

app.run(host="0.0.0.0", port=8000)
 
