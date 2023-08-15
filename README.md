# Bitcoin price prediction

## Инструкции по запуску

Скопировать это репозиторий:
```bash
$ git clone https://github.com/dm1trykrylov/btc-time-series.git
$ cd btc-time-series
```

Чтобы избежать конфликтов версий, лучше перед запуском ноутбука активировать virtual environment :
```bash
$ python3 -m venv venv
$ source venv/bin/activate
```

В начало ноутбука вставлена команда для установки всех зависимостей, можно выполнить её отдельно:
```bash
$ pip3 install -r requirements.txt
```

## Описание ноутбука

Используется модель **DeepAR** из фреймворка **ETNA**.

**Параметры модели:**
```python
DeepARModel(
    encoder_length=7,
    decoder_length=7,
    trainer_params=dict(max_epochs=150, gpus=0, gradient_clip_val=0.1),
    lr=0.01,
    train_batch_size=64,
    rnn_layers=2
)
```

**Преобразования данных**:
* Учёт дня недели
* Лаги от 7 до 11 дней