---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200014"
---
# <span data-ttu-id="a742b-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a742b-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="a742b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a742b-102">SYNOPSIS</span></span>
<span data-ttu-id="a742b-103">Ottiene i dati di livello dei prezzi per Azure Security Center per un ambito.</span><span class="sxs-lookup"><span data-stu-id="a742b-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="a742b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a742b-104">SYNTAX</span></span>

### <span data-ttu-id="a742b-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a742b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a742b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a742b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a742b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a742b-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a742b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a742b-108">DESCRIPTION</span></span>
<span data-ttu-id="a742b-109">Il livello di prezzo del centro di sicurezza di Azure viene deciso per ogni ambito, con questo cmdlet è possibile ottenere i livelli di prezzo configurati.</span><span class="sxs-lookup"><span data-stu-id="a742b-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="a742b-110">Il livello prezzi abbonamento include tutti i gruppi di risorse sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="a742b-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="a742b-111">Il livello di prezzo dei gruppi di risorse sovrascriverà il livello prezzi abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a742b-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="a742b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a742b-112">EXAMPLES</span></span>

### <span data-ttu-id="a742b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a742b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="a742b-114">Ottiene tutti i livelli di prezzo configurati per l'abbonamento e i gruppi di risorse sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="a742b-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="a742b-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a742b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="a742b-116">Ottiene il livello di prezzo configurato per il gruppo di risorse "myService1".</span><span class="sxs-lookup"><span data-stu-id="a742b-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="a742b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a742b-117">PARAMETERS</span></span>

### <span data-ttu-id="a742b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a742b-118">-DefaultProfile</span></span>
<span data-ttu-id="a742b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a742b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a742b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a742b-120">-Name</span></span>
<span data-ttu-id="a742b-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="a742b-121">Resource name.</span></span>

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

### <span data-ttu-id="a742b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a742b-122">-ResourceId</span></span>
<span data-ttu-id="a742b-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a742b-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a742b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a742b-124">CommonParameters</span></span>
<span data-ttu-id="a742b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a742b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a742b-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a742b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a742b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a742b-127">INPUTS</span></span>

### <span data-ttu-id="a742b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a742b-128">System.String</span></span>

## <span data-ttu-id="a742b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a742b-129">OUTPUTS</span></span>

### <span data-ttu-id="a742b-130">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a742b-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="a742b-131">Note</span><span class="sxs-lookup"><span data-stu-id="a742b-131">NOTES</span></span>

## <span data-ttu-id="a742b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a742b-132">RELATED LINKS</span></span>
