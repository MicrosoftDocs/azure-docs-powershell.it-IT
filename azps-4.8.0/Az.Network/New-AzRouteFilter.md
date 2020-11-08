---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192075"
---
# <span data-ttu-id="4a4f3-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a4f3-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="4a4f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4f3-103">Crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-103">Creates a route filter.</span></span>

## <span data-ttu-id="4a4f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a4f3-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a4f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a4f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4a4f3-106">Il cmdlet New-AzRouteFilter crea un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="4a4f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a4f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4a4f3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a4f3-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="4a4f3-109">Il comando crea un nuovo filtro di route.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="4a4f3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a4f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4a4f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a4f3-111">-AsJob</span></span>
<span data-ttu-id="4a4f3-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4a4f3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a4f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4f3-113">-DefaultProfile</span></span>
<span data-ttu-id="4a4f3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a4f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4a4f3-115">-Force</span></span>
<span data-ttu-id="4a4f3-116">Indica che questo cmdlet crea una tabella di route anche se esiste già un filtro di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="4a4f3-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4a4f3-117">-Location</span></span>
<span data-ttu-id="4a4f3-118">Specifica l'area di Azure in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="4a4f3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a4f3-119">-Name</span></span>
<span data-ttu-id="4a4f3-120">Specifica un nome per il filtro della route.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="4a4f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a4f3-122">Specifica il nome del gruppo di risorse in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="4a4f3-123">-Regola</span><span class="sxs-lookup"><span data-stu-id="4a4f3-123">-Rule</span></span>
<span data-ttu-id="4a4f3-124">Specifica una matrice di oggetti della regola del filtro route da associare al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4f3-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a4f3-125">-Tag</span></span>
<span data-ttu-id="4a4f3-126">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4a4f3-127">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4a4f3-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4a4f3-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a4f3-128">-Confirm</span></span>
<span data-ttu-id="4a4f3-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a4f3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a4f3-130">-WhatIf</span></span>
<span data-ttu-id="4a4f3-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a4f3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a4f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4f3-133">CommonParameters</span></span>
<span data-ttu-id="4a4f3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4f3-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4f3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4f3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a4f3-136">INPUTS</span></span>

### <span data-ttu-id="4a4f3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4a4f3-137">System.String</span></span>

### <span data-ttu-id="4a4f3-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="4a4f3-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="4a4f3-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a4f3-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a4f3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a4f3-140">OUTPUTS</span></span>

### <span data-ttu-id="4a4f3-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a4f3-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4a4f3-142">Note</span><span class="sxs-lookup"><span data-stu-id="4a4f3-142">NOTES</span></span>
<span data-ttu-id="4a4f3-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="4a4f3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4a4f3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a4f3-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a4f3-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a4f3-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4a4f3-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a4f3-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4a4f3-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a4f3-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="4a4f3-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4f3-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4a4f3-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4f3-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4a4f3-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4f3-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4a4f3-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4f3-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4a4f3-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4f3-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
