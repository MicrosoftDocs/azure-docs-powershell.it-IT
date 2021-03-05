---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 430f31a0e44f226584d06a341971ed206a2bf5d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006781"
---
# <span data-ttu-id="c431b-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="c431b-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="c431b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c431b-102">SYNOPSIS</span></span>
<span data-ttu-id="c431b-103">Ottiene informazioni su un trigger nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="c431b-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="c431b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c431b-104">SYNTAX</span></span>

### <span data-ttu-id="c431b-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c431b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c431b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c431b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c431b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c431b-107">DESCRIPTION</span></span>
<span data-ttu-id="c431b-108">Il cmdlet **Get-AzDataShareTrigger** ottiene informazioni sul trigger per la sottoscrizione della condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="c431b-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="c431b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c431b-109">EXAMPLES</span></span>

### <span data-ttu-id="c431b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c431b-110">Example 1</span></span>
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

<span data-ttu-id="c431b-111">Questo comando recupera informazioni sull'attivazione di AdsTrigger per la condivisione della sottoscrizione AdsShareSubscription in WikiAds dell'account per la condivisione di dati.</span><span class="sxs-lookup"><span data-stu-id="c431b-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="c431b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c431b-112">PARAMETERS</span></span>

### <span data-ttu-id="c431b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c431b-113">-AccountName</span></span>
<span data-ttu-id="c431b-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c431b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="c431b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c431b-115">-DefaultProfile</span></span>
<span data-ttu-id="c431b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c431b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c431b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c431b-117">-Name</span></span>
<span data-ttu-id="c431b-118">Nome trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c431b-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="c431b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c431b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c431b-120">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c431b-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c431b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c431b-121">-ResourceId</span></span>
<span data-ttu-id="c431b-122">ID risorsa del trigger</span><span class="sxs-lookup"><span data-stu-id="c431b-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="c431b-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c431b-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="c431b-124">Nome della sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c431b-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c431b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c431b-125">CommonParameters</span></span>
<span data-ttu-id="c431b-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c431b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c431b-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c431b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c431b-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c431b-128">INPUTS</span></span>

### <span data-ttu-id="c431b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c431b-129">System.String</span></span>

## <span data-ttu-id="c431b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c431b-130">OUTPUTS</span></span>

### <span data-ttu-id="c431b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="c431b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="c431b-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="c431b-132">NOTES</span></span>

## <span data-ttu-id="c431b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c431b-133">RELATED LINKS</span></span>
