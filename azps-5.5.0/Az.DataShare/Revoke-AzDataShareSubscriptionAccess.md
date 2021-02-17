---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188567"
---
# <span data-ttu-id="79461-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="79461-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="79461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79461-102">SYNOPSIS</span></span>
<span data-ttu-id="79461-103">Revoca l'accesso alla sottoscrizione della condivisione alla condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="79461-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="79461-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79461-104">SYNTAX</span></span>

### <span data-ttu-id="79461-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79461-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79461-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79461-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79461-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79461-107">DESCRIPTION</span></span>
<span data-ttu-id="79461-108">Il cmdlet **Revoke-AzDataShareSubscriptionAccess** concede a una sottoscrizione di condivisione l'accesso alla condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="79461-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="79461-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79461-109">EXAMPLES</span></span>

### <span data-ttu-id="79461-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79461-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="79461-111">Revoca l'accesso all'abbonamento alla condivisione identificato da id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="79461-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="79461-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79461-112">PARAMETERS</span></span>

### <span data-ttu-id="79461-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79461-113">-AccountName</span></span>
<span data-ttu-id="79461-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79461-114">Azure data share account name</span></span>

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

### <span data-ttu-id="79461-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79461-115">-AsJob</span></span>
<span data-ttu-id="79461-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="79461-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79461-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79461-117">-DefaultProfile</span></span>
<span data-ttu-id="79461-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79461-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79461-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79461-119">-ResourceGroupName</span></span>
<span data-ttu-id="79461-120">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79461-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="79461-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79461-121">-ResourceId</span></span>
<span data-ttu-id="79461-122">ID risorsa della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79461-122">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79461-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="79461-123">-ShareName</span></span>
<span data-ttu-id="79461-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="79461-124">Azure data share name</span></span>

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

### <span data-ttu-id="79461-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79461-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="79461-126">ID sottoscrizione di condivisione della sottoscrizione di condivisione del provider</span><span class="sxs-lookup"><span data-stu-id="79461-126">The share subscription id of the provider share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79461-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79461-127">-Confirm</span></span>
<span data-ttu-id="79461-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79461-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79461-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79461-129">-WhatIf</span></span>
<span data-ttu-id="79461-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79461-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79461-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79461-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79461-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79461-132">CommonParameters</span></span>
<span data-ttu-id="79461-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79461-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79461-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79461-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79461-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="79461-135">INPUTS</span></span>

### <span data-ttu-id="79461-136">System.String</span><span class="sxs-lookup"><span data-stu-id="79461-136">System.String</span></span>

## <span data-ttu-id="79461-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79461-137">OUTPUTS</span></span>

### <span data-ttu-id="79461-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="79461-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="79461-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="79461-139">NOTES</span></span>

## <span data-ttu-id="79461-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79461-140">RELATED LINKS</span></span>
