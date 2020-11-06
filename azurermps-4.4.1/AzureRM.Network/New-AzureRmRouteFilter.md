---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513260"
---
# <span data-ttu-id="51c99-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="51c99-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="51c99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51c99-102">SYNOPSIS</span></span>
<span data-ttu-id="51c99-103">Crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="51c99-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51c99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51c99-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51c99-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51c99-105">DESCRIPTION</span></span>
<span data-ttu-id="51c99-106">Il cmdlet New-AzureRmRouteFilter crea un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="51c99-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="51c99-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51c99-107">EXAMPLES</span></span>

### <span data-ttu-id="51c99-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51c99-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="51c99-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="51c99-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="51c99-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51c99-110">PARAMETERS</span></span>

### <span data-ttu-id="51c99-111">-Force</span><span class="sxs-lookup"><span data-stu-id="51c99-111">-Force</span></span>
<span data-ttu-id="51c99-112">Indica che questo cmdlet crea una tabella di route anche se esiste già un filtro di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="51c99-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="51c99-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="51c99-113">-Location</span></span>
<span data-ttu-id="51c99-114">Specifica l'area di Azure in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="51c99-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="51c99-115">-Name</span></span>
<span data-ttu-id="51c99-116">Specifica un nome per il filtro della route.</span><span class="sxs-lookup"><span data-stu-id="51c99-116">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c99-117">-ResourceGroupName</span></span>
<span data-ttu-id="51c99-118">Specifica il nome del gruppo di risorse in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="51c99-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-119">-Regola</span><span class="sxs-lookup"><span data-stu-id="51c99-119">-Rule</span></span>
<span data-ttu-id="51c99-120">Specifica una matrice di oggetti della regola del filtro route da associare al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="51c99-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="51c99-121">-Tag</span></span>
<span data-ttu-id="51c99-122">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="51c99-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51c99-123">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="51c99-123">For example:</span></span>

<span data-ttu-id="51c99-124">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="51c99-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51c99-125">-Confirm</span></span>
<span data-ttu-id="51c99-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51c99-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c99-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c99-127">-WhatIf</span></span>
<span data-ttu-id="51c99-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51c99-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51c99-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51c99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51c99-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c99-130">-DefaultProfile</span></span>
<span data-ttu-id="51c99-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51c99-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c99-132">CommonParameters</span></span>
<span data-ttu-id="51c99-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c99-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c99-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c99-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c99-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51c99-135">INPUTS</span></span>

## <span data-ttu-id="51c99-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51c99-136">OUTPUTS</span></span>

### <span data-ttu-id="51c99-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="51c99-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="51c99-138">Note</span><span class="sxs-lookup"><span data-stu-id="51c99-138">NOTES</span></span>
<span data-ttu-id="51c99-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="51c99-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="51c99-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51c99-140">RELATED LINKS</span></span>

[<span data-ttu-id="51c99-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="51c99-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="51c99-142">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51c99-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="51c99-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="51c99-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="51c99-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="51c99-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
