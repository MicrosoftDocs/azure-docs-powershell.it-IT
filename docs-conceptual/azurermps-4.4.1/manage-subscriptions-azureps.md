---
title: Gestire le sottoscrizioni di Azure con Azure PowerShell | Microsoft Docs
description: Gestire le sottoscrizioni di Azure con Azure PowerShell
keywords: Azure PowerShell, sottoscrizione
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: d2674e37a211d1c1896a13e234cda95beea4479a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243991"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="b2f8f-104">Gestire più sottoscrizioni di Azure</span><span class="sxs-lookup"><span data-stu-id="b2f8f-104">Manage multiple Azure subscriptions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="b2f8f-105">Se si usa Azure da poco, probabilmente si avrà una singola sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="b2f8f-106">Tuttavia, se si usa Azure già da tempo, probabilmente si saranno create più sottoscrizioni di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="b2f8f-107">È possibile configurare Azure PowerShell per eseguire comandi su una determinata sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="b2f8f-108">Ottenere un elenco di tutte le sottoscrizioni dell'account.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="b2f8f-109">Impostare il parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="b2f8f-110">Verificare la modifica eseguendo il cmdlet `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="b2f8f-111">Dopo aver impostato la sottoscrizione predefinita, tutti i successivi comandi di Azure PowerShell verranno eseguiti con questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b2f8f-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
