default:
	@echo "APPC challenge"
	@echo "--------------"
	@echo "Available make commands:"
	@echo ""
	@echo "visit-website \t\t Opens the challenge at Kaggle with default browser"
	@echo "download-data \t\t Downloads data with your browser"
	@echo "unzip-data \t\t Unzips downloaded data"

downloader=wget -nc --directory-prefix=data
unzipper=unzip -n -d data

visit-website:
	@echo "Opening the website"
	@xdg-open https://www.kaggle.com/c/allstate-purchase-prediction-challenge

download-data:
	@mkdir -p data
	@echo "Downloading data with your browser..."
	@xdg-open https://www.kaggle.com/c/allstate-purchase-prediction-challenge/download/sampleSubmission.csv
	@xdg-open https://www.kaggle.com/c/allstate-purchase-prediction-challenge/download/train.csv.zip
	@xdg-open https://www.kaggle.com/c/allstate-purchase-prediction-challenge/download/test_v2.csv.zip
	@echo "Once downloaded put to the data directory"

unzip-data:
	@mkdir -p data
	$(unzipper) data/train.csv.zip
	$(unzipper) data/test_v2.csv.zip
