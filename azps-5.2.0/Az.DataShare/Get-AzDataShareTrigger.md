---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324447"
---
# <span data-ttu-id="122f3-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="122f3-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="122f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="122f3-102">SYNOPSIS</span></span>
<span data-ttu-id="122f3-103">Ottiene le informazioni su un trigger nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="122f3-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="122f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="122f3-104">SYNTAX</span></span>

### <span data-ttu-id="122f3-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="122f3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="122f3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="122f3-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="122f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="122f3-107">DESCRIPTION</span></span>
<span data-ttu-id="122f3-108">Il cmdlet **Get-AzDataShareTrigger** ottiene le informazioni sul trigger per l'abbonamento alla condivisione in account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="122f3-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="122f3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="122f3-109">EXAMPLES</span></span>

### <span data-ttu-id="122f3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="122f3-110">Example 1</span></span>
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

<span data-ttu-id="122f3-111">Questo comando consente di ottenere informazioni su trigger AdsTrigger per l'abbonamento alla condivisione AdsShareSubscription in WikiAds account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="122f3-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="122f3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="122f3-112">PARAMETERS</span></span>

### <span data-ttu-id="122f3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="122f3-113">-AccountName</span></span>
<span data-ttu-id="122f3-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="122f3-114">Azure data share account name</span></span>

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

### <span data-ttu-id="122f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122f3-115">-DefaultProfile</span></span>
<span data-ttu-id="122f3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="122f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="122f3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="122f3-117">-Name</span></span>
<span data-ttu-id="122f3-118">Nome del trigger di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="122f3-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="122f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="122f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="122f3-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="122f3-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="122f3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="122f3-121">-ResourceId</span></span>
<span data-ttu-id="122f3-122">ID risorsa del trigger</span><span class="sxs-lookup"><span data-stu-id="122f3-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="122f3-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="122f3-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="122f3-124">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="122f3-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="122f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122f3-125">CommonParameters</span></span>
<span data-ttu-id="122f3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122f3-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="122f3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122f3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="122f3-128">INPUTS</span></span>

### <span data-ttu-id="122f3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="122f3-129">System.String</span></span>

## <span data-ttu-id="122f3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="122f3-130">OUTPUTS</span></span>

### <span data-ttu-id="122f3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="122f3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="122f3-132">Note</span><span class="sxs-lookup"><span data-stu-id="122f3-132">NOTES</span></span>

## <span data-ttu-id="122f3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="122f3-133">RELATED LINKS</span></span>
