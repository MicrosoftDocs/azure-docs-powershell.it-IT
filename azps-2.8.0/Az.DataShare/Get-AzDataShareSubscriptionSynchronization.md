---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 62b0a959e632c3e54b07e9238ae4ea9034a7408b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674684"
---
# <span data-ttu-id="67e99-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="67e99-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="67e99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67e99-102">SYNOPSIS</span></span>
<span data-ttu-id="67e99-103">Ottiene le informazioni sulla sincronizzazione eseguito in Condividi abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67e99-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="67e99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67e99-104">SYNTAX</span></span>

### <span data-ttu-id="67e99-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67e99-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67e99-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e99-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67e99-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67e99-107">DESCRIPTION</span></span>
<span data-ttu-id="67e99-108">Il cmdlet **Get-AzDataShareSubscriptionSynchronization** fornisce informaiton su tutte le operazioni di sincronizzazione eseguite in un abbonamento a una condivisione in un account di condivisione dati nel consumer.</span><span class="sxs-lookup"><span data-stu-id="67e99-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="67e99-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67e99-109">EXAMPLES</span></span>

### <span data-ttu-id="67e99-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67e99-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="67e99-111">Questo comando fornisce informazioni su tutte le esecuzioni della sincronizzazione per un abbonamento a AdsShareSubscription in account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="67e99-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="67e99-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67e99-112">PARAMETERS</span></span>

### <span data-ttu-id="67e99-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67e99-113">-AccountName</span></span>
<span data-ttu-id="67e99-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67e99-114">Azure data share account name</span></span>

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

### <span data-ttu-id="67e99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e99-115">-DefaultProfile</span></span>
<span data-ttu-id="67e99-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67e99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e99-117">-ResourceGroupName</span></span>
<span data-ttu-id="67e99-118">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67e99-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="67e99-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67e99-119">-ResourceId</span></span>
<span data-ttu-id="67e99-120">ID risorsa di abbonamento a Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="67e99-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="67e99-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="67e99-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="67e99-122">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67e99-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="67e99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e99-123">CommonParameters</span></span>
<span data-ttu-id="67e99-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e99-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e99-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e99-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67e99-126">INPUTS</span></span>

### <span data-ttu-id="67e99-127">System. String</span><span class="sxs-lookup"><span data-stu-id="67e99-127">System.String</span></span>

## <span data-ttu-id="67e99-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67e99-128">OUTPUTS</span></span>

### <span data-ttu-id="67e99-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="67e99-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="67e99-130">Note</span><span class="sxs-lookup"><span data-stu-id="67e99-130">NOTES</span></span>

## <span data-ttu-id="67e99-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67e99-131">RELATED LINKS</span></span>
