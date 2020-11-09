---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297505"
---
# <span data-ttu-id="79959-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="79959-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="79959-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79959-102">SYNOPSIS</span></span>
<span data-ttu-id="79959-103">Ottiene le informazioni sulla sincronizzazione eseguito in Condividi abbonamento.</span><span class="sxs-lookup"><span data-stu-id="79959-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="79959-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79959-104">SYNTAX</span></span>

### <span data-ttu-id="79959-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79959-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79959-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79959-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79959-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79959-107">DESCRIPTION</span></span>
<span data-ttu-id="79959-108">Il cmdlet **Get-AzDataShareSubscriptionSynchronization** fornisce informaiton su tutte le operazioni di sincronizzazione eseguite in un abbonamento a una condivisione in un account di condivisione dati nel consumer.</span><span class="sxs-lookup"><span data-stu-id="79959-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="79959-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79959-109">EXAMPLES</span></span>

### <span data-ttu-id="79959-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79959-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="79959-111">Questo comando fornisce informazioni su tutte le esecuzioni della sincronizzazione per un abbonamento a AdsShareSubscription in account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="79959-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="79959-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79959-112">PARAMETERS</span></span>

### <span data-ttu-id="79959-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79959-113">-AccountName</span></span>
<span data-ttu-id="79959-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79959-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79959-115">-DefaultProfile</span></span>
<span data-ttu-id="79959-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79959-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79959-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79959-117">-ResourceGroupName</span></span>
<span data-ttu-id="79959-118">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79959-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79959-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79959-119">-ResourceId</span></span>
<span data-ttu-id="79959-120">ID risorsa di abbonamento a Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="79959-120">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79959-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="79959-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="79959-122">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79959-122">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79959-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79959-123">CommonParameters</span></span>
<span data-ttu-id="79959-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79959-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79959-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79959-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79959-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79959-126">INPUTS</span></span>

### <span data-ttu-id="79959-127">System. String</span><span class="sxs-lookup"><span data-stu-id="79959-127">System.String</span></span>

## <span data-ttu-id="79959-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79959-128">OUTPUTS</span></span>

### <span data-ttu-id="79959-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="79959-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="79959-130">Note</span><span class="sxs-lookup"><span data-stu-id="79959-130">NOTES</span></span>

## <span data-ttu-id="79959-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79959-131">RELATED LINKS</span></span>
