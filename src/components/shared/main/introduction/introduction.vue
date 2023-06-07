<template>
    <div class="main-introduction">
        <div class="main-introduction__info">
            <h1 class="main-introduction__info-title">Fitness as a service</h1>

            <p class="main-introduction__info-label">
                for hotels and properties
            </p>

            <p class="main-introduction__info-description">
                We offer exclusive private and group fitness experiences for
                your guests, using your hotel facilities under your hotel's
                brand and cutting-edge digital technologies. We confidently
                maintain your high standards of service, ensuring that your
                guests receive the best possible experience
            </p>
        </div>

        <div class="main-introduction__contacts">
            <div class="main-introduction__contacts-links">
                <a
                    class="main-introduction__contacts-email"
                    href="mailto:goahead@labelsports.ae"
                >
                    goahead@labelsports.ae
                </a>

                <a
                    class="main-introduction__contacts-phone"
                    href="tel:+971521686850"
                >
                    +971 52 168 6850
                </a>
            </div>

            <p class="main-introduction__contacts-location">
                🇦🇪 DUBAI, DIC, in5Tech
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: "MainIntroduction",
};
</script>

<style lang="scss">
.main-introduction {
    width: 100%;
    padding: 80px 130px 80px 135px;

    .main-introduction__info {
        margin-bottom: 210px;
    }

    .main-introduction__info-title {
        font-size: 56px;
        line-height: 60px;
    }

    .main-introduction__info-label {
        @include montserrat-medium;
        font-size: 28px;
        line-height: 32px;
        margin: 20px 0 32px 0;
    }

    .main-introduction__info-description {
        @include inter-regular;
        font-size: 18px;
        line-height: 28px;
        color: $txt-light;
    }

    .main-introduction__contacts {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        grid-row-gap: 24px;
    }

    .main-introduction__contacts-links {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        grid-row-gap: 12px;
    }

    .main-introduction__contacts-email {
        @include inter-regular;
        font-size: 18px;
        line-height: 24px;
        color: $txt-primary;
    }

    .main-introduction__contacts-phone {
        @include inter-semi-bold;
        font-size: 18px;
        line-height: 24px;
        color: $txt-main;
    }

    .main-introduction__contacts-location {
        @include inter-regular;
        font-size: 14px;
        line-height: 18px;
    }
}

@media screen and (max-width: 1440px) {
    .main-introduction {
        padding-inline: 60px;
    }
}

@media screen and (max-width: 768px) {
    .main-introduction {
        padding: 32px 20px;

        .main-introduction__info {
            margin-bottom: 166px;
        }

        .main-introduction__info-title {
            font-size: 34px;
            line-height: 38px;
        }

        .main-introduction__info-label {
            font-size: 20px;
            line-height: 24px;
            margin: 12px 0 24px 0;
        }

        .main-introduction__info-description {
            font-size: 18px;
            line-height: 28px;
        }

        .main-introduction__contacts {
            flex-direction: row;
            align-items: flex-end;
            grid-column-gap: 35px;
        }

        .main-introduction__contacts-email {
            font-size: 14px;
            line-height: 18px;
        }

        .main-introduction__contacts-phone {
            font-size: 14px;
            line-height: 18px;
        }

        .main-introduction__contacts-location {
            font-size: 14px;
            line-height: 18px;
            white-space: nowrap;
        }
    }
}
</style>
