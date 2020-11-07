---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: a28fe30424b5b1d29c3b671e5cec266fc75d9dbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520166"
---
# <span data-ttu-id="24060-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="24060-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="24060-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24060-102">SYNOPSIS</span></span>
<span data-ttu-id="24060-103">Crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="24060-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24060-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24060-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24060-105">DESCRIPTION</span></span>
<span data-ttu-id="24060-106">Il cmdlet New-AzureRmRouteFilter crea un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="24060-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="24060-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24060-107">EXAMPLES</span></span>

### <span data-ttu-id="24060-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24060-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="24060-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="24060-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="24060-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24060-110">PARAMETERS</span></span>

### <span data-ttu-id="24060-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24060-111">-AsJob</span></span>
<span data-ttu-id="24060-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="24060-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24060-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24060-113">-DefaultProfile</span></span>
<span data-ttu-id="24060-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24060-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24060-115">-Force</span><span class="sxs-lookup"><span data-stu-id="24060-115">-Force</span></span>
<span data-ttu-id="24060-116">Indica che questo cmdlet crea una tabella di route anche se esiste già un filtro di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="24060-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="24060-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24060-117">-Location</span></span>
<span data-ttu-id="24060-118">Specifica l'area di Azure in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="24060-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="24060-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="24060-119">-Name</span></span>
<span data-ttu-id="24060-120">Specifica un nome per il filtro della route.</span><span class="sxs-lookup"><span data-stu-id="24060-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="24060-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24060-121">-ResourceGroupName</span></span>
<span data-ttu-id="24060-122">Specifica il nome del gruppo di risorse in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="24060-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="24060-123">-Regola</span><span class="sxs-lookup"><span data-stu-id="24060-123">-Rule</span></span>
<span data-ttu-id="24060-124">Specifica una matrice di oggetti della regola del filtro route da associare al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="24060-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="24060-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="24060-125">-Tag</span></span>
<span data-ttu-id="24060-126">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="24060-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24060-127">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="24060-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24060-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24060-128">-Confirm</span></span>
<span data-ttu-id="24060-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24060-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24060-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24060-130">-WhatIf</span></span>
<span data-ttu-id="24060-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24060-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24060-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24060-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24060-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24060-133">CommonParameters</span></span>
<span data-ttu-id="24060-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24060-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24060-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24060-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24060-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24060-136">INPUTS</span></span>

### <span data-ttu-id="24060-137">System. String</span><span class="sxs-lookup"><span data-stu-id="24060-137">System.String</span></span>

### <span data-ttu-id="24060-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="24060-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="24060-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24060-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24060-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24060-140">OUTPUTS</span></span>

### <span data-ttu-id="24060-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="24060-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="24060-142">Note</span><span class="sxs-lookup"><span data-stu-id="24060-142">NOTES</span></span>
<span data-ttu-id="24060-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="24060-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="24060-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24060-144">RELATED LINKS</span></span>

[<span data-ttu-id="24060-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="24060-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="24060-146">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24060-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="24060-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="24060-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="24060-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="24060-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)