---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 93e0aa57a418af038a397559959b40500ad58af3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674640"
---
# <span data-ttu-id="cb0b2-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="cb0b2-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="cb0b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0b2-103">Revoca l'accesso all'abbonamento alla condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="cb0b2-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="cb0b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb0b2-104">SYNTAX</span></span>

### <span data-ttu-id="cb0b2-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb0b2-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb0b2-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb0b2-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb0b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb0b2-107">DESCRIPTION</span></span>
<span data-ttu-id="cb0b2-108">Il cmdlet **Revoke-AzDataShareSubscriptionAccess** concede a un abbonamento di condivisione l'accesso alla condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="cb0b2-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="cb0b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb0b2-109">EXAMPLES</span></span>

### <span data-ttu-id="cb0b2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb0b2-110">Example 1</span></span>
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

<span data-ttu-id="cb0b2-111">Revoca l'accesso dell'abbonamento alla condivisione identificato da ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="cb0b2-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="cb0b2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb0b2-112">PARAMETERS</span></span>

### <span data-ttu-id="cb0b2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb0b2-113">-AccountName</span></span>
<span data-ttu-id="cb0b2-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="cb0b2-114">Azure data share account name</span></span>

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

### <span data-ttu-id="cb0b2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb0b2-115">-AsJob</span></span>
<span data-ttu-id="cb0b2-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="cb0b2-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="cb0b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0b2-117">-DefaultProfile</span></span>
<span data-ttu-id="cb0b2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb0b2-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="cb0b2-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cb0b2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb0b2-121">-ResourceId</span></span>
<span data-ttu-id="cb0b2-122">ID risorsa della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="cb0b2-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="cb0b2-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cb0b2-123">-ShareName</span></span>
<span data-ttu-id="cb0b2-124">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="cb0b2-124">Azure data share name</span></span>

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

### <span data-ttu-id="cb0b2-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb0b2-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="cb0b2-126">ID condivisione sottoscrizione dell'abbonamento alla condivisione del provider</span><span class="sxs-lookup"><span data-stu-id="cb0b2-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="cb0b2-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb0b2-127">-Confirm</span></span>
<span data-ttu-id="cb0b2-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb0b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb0b2-129">-WhatIf</span></span>
<span data-ttu-id="cb0b2-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb0b2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb0b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0b2-132">CommonParameters</span></span>
<span data-ttu-id="cb0b2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0b2-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0b2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0b2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb0b2-135">INPUTS</span></span>

### <span data-ttu-id="cb0b2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb0b2-136">System.String</span></span>

## <span data-ttu-id="cb0b2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb0b2-137">OUTPUTS</span></span>

### <span data-ttu-id="cb0b2-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="cb0b2-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="cb0b2-139">Note</span><span class="sxs-lookup"><span data-stu-id="cb0b2-139">NOTES</span></span>

## <span data-ttu-id="cb0b2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb0b2-140">RELATED LINKS</span></span>