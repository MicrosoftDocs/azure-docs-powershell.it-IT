---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486260"
---
# <span data-ttu-id="2fc65-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2fc65-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="2fc65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fc65-102">SYNOPSIS</span></span>

<span data-ttu-id="2fc65-103">Abilita o Disabilita i piani di Azure Defender per un abbonamento in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="2fc65-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="2fc65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fc65-104">SYNTAX</span></span>

### <span data-ttu-id="2fc65-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fc65-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc65-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc65-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc65-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fc65-107">DESCRIPTION</span></span>

<span data-ttu-id="2fc65-108">Abilitare o disabilitare i piani di Azure Defender per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2fc65-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="2fc65-109">Per informazioni dettagliate su Azure Defender e sui piani disponibili, vedere [Introduzione a Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="2fc65-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="2fc65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fc65-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc65-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2fc65-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="2fc65-112">Abilita **Azure Defender per i server** per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2fc65-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="2fc65-113">"Standard" si riferisce allo stato "on" per un piano di Azure Defender, come illustrato nell'area dei prezzi e delle impostazioni di Azure Security Center di Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="2fc65-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="2fc65-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fc65-114">PARAMETERS</span></span>

### <span data-ttu-id="2fc65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc65-115">-DefaultProfile</span></span>

<span data-ttu-id="2fc65-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc65-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc65-117">-InputObject</span></span>

<span data-ttu-id="2fc65-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="2fc65-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc65-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fc65-119">-Name</span></span>

<span data-ttu-id="2fc65-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="2fc65-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc65-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="2fc65-121">-PricingTier</span></span>

<span data-ttu-id="2fc65-122">Livello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="2fc65-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc65-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fc65-123">-Confirm</span></span>

<span data-ttu-id="2fc65-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fc65-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc65-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc65-125">-WhatIf</span></span>

<span data-ttu-id="2fc65-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fc65-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fc65-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fc65-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc65-128">CommonParameters</span></span>

<span data-ttu-id="2fc65-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc65-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fc65-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc65-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fc65-131">INPUTS</span></span>

### <span data-ttu-id="2fc65-132">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2fc65-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2fc65-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fc65-133">OUTPUTS</span></span>

### <span data-ttu-id="2fc65-134">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2fc65-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2fc65-135">Note</span><span class="sxs-lookup"><span data-stu-id="2fc65-135">NOTES</span></span>

## <span data-ttu-id="2fc65-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fc65-136">RELATED LINKS</span></span>
