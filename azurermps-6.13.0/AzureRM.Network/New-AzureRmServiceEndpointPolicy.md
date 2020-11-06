---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520165"
---
# <span data-ttu-id="ad693-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad693-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="ad693-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad693-102">SYNOPSIS</span></span>
<span data-ttu-id="ad693-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="ad693-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad693-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad693-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad693-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad693-105">DESCRIPTION</span></span>
<span data-ttu-id="ad693-106">Il cmdlet **New-AzureRmServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="ad693-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="ad693-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad693-107">EXAMPLES</span></span>

### <span data-ttu-id="ad693-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="ad693-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="ad693-109">Questo comando crea un criterio endpoint del servizio denominato Policy1 con le definizioni definite dall'oggetto $serviceEndpointDefinition e lo archivia nella variabile $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad693-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="ad693-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad693-110">PARAMETERS</span></span>

### <span data-ttu-id="ad693-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad693-111">-DefaultProfile</span></span>
<span data-ttu-id="ad693-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad693-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad693-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ad693-113">-Force</span></span>
<span data-ttu-id="ad693-114">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="ad693-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad693-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad693-115">-Name</span></span>
<span data-ttu-id="ad693-116">Nome della subnet</span><span class="sxs-lookup"><span data-stu-id="ad693-116">The name of the subnet</span></span>

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

### <span data-ttu-id="ad693-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad693-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad693-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad693-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad693-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="ad693-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="ad693-120">Elenco di definizioni di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="ad693-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad693-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad693-121">-Confirm</span></span>
<span data-ttu-id="ad693-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad693-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad693-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad693-123">-WhatIf</span></span>
<span data-ttu-id="ad693-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad693-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad693-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad693-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad693-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad693-126">CommonParameters</span></span>
<span data-ttu-id="ad693-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad693-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ad693-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad693-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad693-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad693-129">INPUTS</span></span>

### <span data-ttu-id="ad693-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ad693-130">System.String</span></span>


## <span data-ttu-id="ad693-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad693-131">OUTPUTS</span></span>

### <span data-ttu-id="ad693-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad693-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="ad693-133">Note</span><span class="sxs-lookup"><span data-stu-id="ad693-133">NOTES</span></span>

## <span data-ttu-id="ad693-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad693-134">RELATED LINKS</span></span>
