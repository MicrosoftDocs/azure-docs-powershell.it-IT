---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852725"
---
# <span data-ttu-id="d113f-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d113f-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="d113f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d113f-102">SYNOPSIS</span></span>
<span data-ttu-id="d113f-103">Rimuove un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="d113f-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="d113f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d113f-104">SYNTAX</span></span>

### <span data-ttu-id="d113f-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d113f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d113f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d113f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d113f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d113f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d113f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d113f-108">DESCRIPTION</span></span>
<span data-ttu-id="d113f-109">Il cmdlet **Remove-AzPublicIpPrefix** rimuove un prefisso IP pubblico di Azure purché non siano stati assegnati indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="d113f-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="d113f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d113f-110">EXAMPLES</span></span>

### <span data-ttu-id="d113f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d113f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="d113f-112">Rimuove il prefisso IP pubblico con il nome $prefixName dal gruppo di risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="d113f-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="d113f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d113f-113">PARAMETERS</span></span>

### <span data-ttu-id="d113f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d113f-114">-AsJob</span></span>
<span data-ttu-id="d113f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d113f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d113f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d113f-116">-DefaultProfile</span></span>
<span data-ttu-id="d113f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d113f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d113f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d113f-118">-Force</span></span>
<span data-ttu-id="d113f-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d113f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d113f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d113f-120">-InputObject</span></span>
<span data-ttu-id="d113f-121">Un oggetto PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d113f-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d113f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d113f-122">-Name</span></span>
<span data-ttu-id="d113f-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d113f-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d113f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d113f-124">-PassThru</span></span>
<span data-ttu-id="d113f-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d113f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d113f-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d113f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d113f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d113f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d113f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d113f-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d113f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d113f-129">-ResourceId</span></span>
<span data-ttu-id="d113f-130">ResourceId per la risorsa da rimuovere</span><span class="sxs-lookup"><span data-stu-id="d113f-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d113f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d113f-131">-Confirm</span></span>
<span data-ttu-id="d113f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d113f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d113f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d113f-133">-WhatIf</span></span>
<span data-ttu-id="d113f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d113f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d113f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d113f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d113f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d113f-136">CommonParameters</span></span>
<span data-ttu-id="d113f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d113f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d113f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d113f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d113f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d113f-139">INPUTS</span></span>

### <span data-ttu-id="d113f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d113f-140">System.String</span></span>

### <span data-ttu-id="d113f-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d113f-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="d113f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d113f-142">OUTPUTS</span></span>

### <span data-ttu-id="d113f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d113f-143">System.Boolean</span></span>

## <span data-ttu-id="d113f-144">Note</span><span class="sxs-lookup"><span data-stu-id="d113f-144">NOTES</span></span>

## <span data-ttu-id="d113f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d113f-145">RELATED LINKS</span></span>

[<span data-ttu-id="d113f-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d113f-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="d113f-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d113f-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="d113f-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d113f-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
