---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687291"
---
# <span data-ttu-id="17aaf-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="17aaf-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="17aaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="17aaf-103">Aggiunge una definizione di criteri endpoint servizio a un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="17aaf-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17aaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17aaf-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17aaf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17aaf-105">DESCRIPTION</span></span>
<span data-ttu-id="17aaf-106">Il cmdlet **Add-AzureRmServiceEndpointPolicyDefinition** aggiunge una definizione di criteri endpoint del servizio al criterio.</span><span class="sxs-lookup"><span data-stu-id="17aaf-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="17aaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17aaf-107">EXAMPLES</span></span>

### <span data-ttu-id="17aaf-108">Esempio 1: aggiorna una definizione dei criteri endpoint del servizio in un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="17aaf-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="17aaf-109">Questo comando ha aggiornato la definizione dei criteri endpoint del servizio con Name ServiceEndpointPolicyDefinition1, Service Microsoft. storage, Service Resources subscriptions/Sub1 e Description "New Definition" che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="17aaf-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="17aaf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17aaf-110">PARAMETERS</span></span>

### <span data-ttu-id="17aaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17aaf-111">-DefaultProfile</span></span>
<span data-ttu-id="17aaf-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17aaf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaf-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="17aaf-113">-Description</span></span>
<span data-ttu-id="17aaf-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="17aaf-114">The description of the definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="17aaf-115">-Name</span></span>
<span data-ttu-id="17aaf-116">Nome della definizione dei criteri di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="17aaf-116">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaf-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="17aaf-117">-Service</span></span>
<span data-ttu-id="17aaf-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="17aaf-118">Name of the service</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaf-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="17aaf-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="17aaf-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="17aaf-120">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17aaf-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="17aaf-121">-ServiceResource</span></span>
<span data-ttu-id="17aaf-122">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="17aaf-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17aaf-123">CommonParameters</span></span>
<span data-ttu-id="17aaf-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17aaf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="17aaf-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17aaf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17aaf-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17aaf-126">INPUTS</span></span>

### <span data-ttu-id="17aaf-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="17aaf-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="17aaf-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17aaf-128">OUTPUTS</span></span>

### <span data-ttu-id="17aaf-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="17aaf-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="17aaf-130">Note</span><span class="sxs-lookup"><span data-stu-id="17aaf-130">NOTES</span></span>

## <span data-ttu-id="17aaf-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17aaf-131">RELATED LINKS</span></span>
