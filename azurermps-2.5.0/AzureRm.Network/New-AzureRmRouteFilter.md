---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 981ef70f711cf418a92d8fb0caaae22c114f96b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866873"
---
# <span data-ttu-id="98cb2-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98cb2-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="98cb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="98cb2-103">Crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="98cb2-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98cb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98cb2-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98cb2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="98cb2-106">Il cmdlet New-AzureRmRouteFilter crea un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="98cb2-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="98cb2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98cb2-107">EXAMPLES</span></span>

### <span data-ttu-id="98cb2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98cb2-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="98cb2-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="98cb2-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="98cb2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98cb2-110">PARAMETERS</span></span>

### <span data-ttu-id="98cb2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98cb2-111">-AsJob</span></span>
<span data-ttu-id="98cb2-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="98cb2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98cb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98cb2-113">-DefaultProfile</span></span>
<span data-ttu-id="98cb2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98cb2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98cb2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="98cb2-115">-Force</span></span>
<span data-ttu-id="98cb2-116">Indica che questo cmdlet crea una tabella di route anche se esiste già un filtro di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="98cb2-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="98cb2-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="98cb2-117">-Location</span></span>
<span data-ttu-id="98cb2-118">Specifica l'area di Azure in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="98cb2-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="98cb2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="98cb2-119">-Name</span></span>
<span data-ttu-id="98cb2-120">Specifica un nome per il filtro della route.</span><span class="sxs-lookup"><span data-stu-id="98cb2-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="98cb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98cb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="98cb2-122">Specifica il nome del gruppo di risorse in cui questo cmdlet crea un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="98cb2-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="98cb2-123">-Regola</span><span class="sxs-lookup"><span data-stu-id="98cb2-123">-Rule</span></span>
<span data-ttu-id="98cb2-124">Specifica una matrice di oggetti della regola del filtro route da associare al filtro della route.</span><span class="sxs-lookup"><span data-stu-id="98cb2-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="98cb2-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="98cb2-125">-Tag</span></span>
<span data-ttu-id="98cb2-126">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="98cb2-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="98cb2-127">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="98cb2-127">For example:</span></span>

<span data-ttu-id="98cb2-128">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="98cb2-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="98cb2-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98cb2-129">-Confirm</span></span>
<span data-ttu-id="98cb2-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98cb2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98cb2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98cb2-131">-WhatIf</span></span>
<span data-ttu-id="98cb2-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98cb2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98cb2-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98cb2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98cb2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98cb2-134">CommonParameters</span></span>
<span data-ttu-id="98cb2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98cb2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98cb2-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98cb2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98cb2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98cb2-137">INPUTS</span></span>

## <span data-ttu-id="98cb2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98cb2-138">OUTPUTS</span></span>

### <span data-ttu-id="98cb2-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98cb2-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="98cb2-140">Note</span><span class="sxs-lookup"><span data-stu-id="98cb2-140">NOTES</span></span>
<span data-ttu-id="98cb2-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="98cb2-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="98cb2-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98cb2-142">RELATED LINKS</span></span>

[<span data-ttu-id="98cb2-143">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98cb2-143">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="98cb2-144">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98cb2-144">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="98cb2-145">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98cb2-145">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="98cb2-146">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98cb2-146">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
