---
title: Gestire le sottoscrizioni di Azure con Azure PowerShell | Microsoft Docs
description: Gestire le sottoscrizioni di Azure con Azure PowerShell
keywords: Azure PowerShell, sottoscrizione
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 8869b700e513d6fc07e69de1dbfe852bd2a52df1
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576267"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="60a66-104">Gestire più sottoscrizioni di Azure</span><span class="sxs-lookup"><span data-stu-id="60a66-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="60a66-105">Se si usa Azure da poco, probabilmente si avrà una singola sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="60a66-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="60a66-106">Tuttavia, se si usa Azure già da tempo, probabilmente si saranno create più sottoscrizioni di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a66-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="60a66-107">È possibile configurare Azure PowerShell per eseguire comandi su una determinata sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="60a66-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="60a66-108">Ottenere un elenco di tutte le sottoscrizioni dell'account.</span><span class="sxs-lookup"><span data-stu-id="60a66-108">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="60a66-109">Impostare il parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="60a66-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="60a66-110">Verificare la modifica eseguendo il cmdlet `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="60a66-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="60a66-111">Dopo aver impostato la sottoscrizione predefinita, tutti i successivi comandi di Azure PowerShell verranno eseguiti con questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="60a66-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
