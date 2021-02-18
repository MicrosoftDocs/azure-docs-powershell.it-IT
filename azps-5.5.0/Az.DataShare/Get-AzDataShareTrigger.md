---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200542"
---
# <span data-ttu-id="82e22-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="82e22-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="82e22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e22-102">SYNOPSIS</span></span>
<span data-ttu-id="82e22-103">Ottiene informazioni su un trigger nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="82e22-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="82e22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82e22-104">SYNTAX</span></span>

### <span data-ttu-id="82e22-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82e22-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82e22-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e22-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e22-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82e22-107">DESCRIPTION</span></span>
<span data-ttu-id="82e22-108">Il cmdlet **Get-AzDataShareTrigger** ottiene informazioni sul trigger per la sottoscrizione della condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="82e22-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="82e22-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82e22-109">EXAMPLES</span></span>

### <span data-ttu-id="82e22-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82e22-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="82e22-111">Questo comando recupera informazioni sul trigger AdsTrigger per la condivisione dell'abbonamento AdsShareSubscription nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="82e22-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="82e22-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82e22-112">PARAMETERS</span></span>

### <span data-ttu-id="82e22-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82e22-113">-AccountName</span></span>
<span data-ttu-id="82e22-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="82e22-114">Azure data share account name</span></span>

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

### <span data-ttu-id="82e22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e22-115">-DefaultProfile</span></span>
<span data-ttu-id="82e22-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82e22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e22-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82e22-117">-Name</span></span>
<span data-ttu-id="82e22-118">Nome trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="82e22-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e22-119">-ResourceGroupName</span></span>
<span data-ttu-id="82e22-120">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="82e22-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="82e22-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82e22-121">-ResourceId</span></span>
<span data-ttu-id="82e22-122">ID risorsa del trigger</span><span class="sxs-lookup"><span data-stu-id="82e22-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="82e22-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="82e22-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="82e22-124">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="82e22-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="82e22-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e22-125">CommonParameters</span></span>
<span data-ttu-id="82e22-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e22-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e22-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82e22-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e22-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="82e22-128">INPUTS</span></span>

### <span data-ttu-id="82e22-129">System.String</span><span class="sxs-lookup"><span data-stu-id="82e22-129">System.String</span></span>

## <span data-ttu-id="82e22-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82e22-130">OUTPUTS</span></span>

### <span data-ttu-id="82e22-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="82e22-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="82e22-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="82e22-132">NOTES</span></span>

## <span data-ttu-id="82e22-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82e22-133">RELATED LINKS</span></span>
