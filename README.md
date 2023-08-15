# Bitcoin price prediction

Перед запуском ноутбука необходимо установить зависимости:
```bash
pip3 install -r requirements.txt
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