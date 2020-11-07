---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860434"
---
# <span data-ttu-id="b516c-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b516c-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="b516c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b516c-102">SYNOPSIS</span></span>
<span data-ttu-id="b516c-103">Crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="b516c-103">Creates a route filter.</span></span>

## <span data-ttu-id="b516c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b516c-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b516c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b516c-105">DESCRIPTION</span></span>
<span data-ttu-id="b516c-106">Il cmdlet New-AzRouteFilter crea un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="b516c-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="b516c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b516c-107">EXAMPLES</span></span>

### <span data-ttu-id="b516c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b516c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="b516c-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="b516c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b516c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b516c-110">PARAMETERS</span></span>

### <span data-ttu-id="b516c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b516c-111">-AsJob</span></span>
<span data-ttu-id="b516c-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b516c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b516c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b516c-113">-DefaultProfile</span></span>
<span data-ttu-id="b516c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b516c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b516c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b516c-115">-Force</span></span>
<span data-ttu-id="b516c-116">Indica che questo cmdlet crea una tabella di route anche se esiste già un filtro di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b516c-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="b516c-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b516c-117">-Location</span></span>
<span data-ttu-id="b516c-118">Specifica l'area di Azure in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="b516c-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="b516c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b516c-119">-Name</span></span>
<span data-ttu-id="b516c-120">Specifica un nome per il filtro della route.</span><span class="sxs-lookup"><span data-stu-id="b516c-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b516c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b516c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b516c-122">Specifica il nome del gruppo di risorse in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="b516c-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="b516c-123">-Regola</span><span class="sxs-lookup"><span data-stu-id="b516c-123">-Rule</span></span>
<span data-ttu-id="b516c-124">Specifica una matrice di oggetti della regola del filtro route da associare al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="b516c-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="b516c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b516c-125">-Tag</span></span>
<span data-ttu-id="b516c-126">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b516c-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b516c-127">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b516c-127">For example:</span></span>

<span data-ttu-id="b516c-128">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b516c-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b516c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b516c-129">-Confirm</span></span>
<span data-ttu-id="b516c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b516c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b516c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b516c-131">-WhatIf</span></span>
<span data-ttu-id="b516c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b516c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b516c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b516c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b516c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b516c-134">CommonParameters</span></span>
<span data-ttu-id="b516c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b516c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b516c-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b516c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b516c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b516c-137">INPUTS</span></span>

## <span data-ttu-id="b516c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b516c-138">OUTPUTS</span></span>

### <span data-ttu-id="b516c-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b516c-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b516c-140">Note</span><span class="sxs-lookup"><span data-stu-id="b516c-140">NOTES</span></span>
<span data-ttu-id="b516c-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="b516c-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b516c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b516c-142">RELATED LINKS</span></span>

[<span data-ttu-id="b516c-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b516c-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b516c-144">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b516c-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b516c-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b516c-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b516c-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b516c-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
