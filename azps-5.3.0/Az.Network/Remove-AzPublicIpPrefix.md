---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488950"
---
# <span data-ttu-id="c64f1-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c64f1-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="c64f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c64f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c64f1-103">Rimuove un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="c64f1-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="c64f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c64f1-104">SYNTAX</span></span>

### <span data-ttu-id="c64f1-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c64f1-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c64f1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c64f1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c64f1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c64f1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c64f1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c64f1-108">DESCRIPTION</span></span>
<span data-ttu-id="c64f1-109">Il cmdlet **Remove-AzPublicIpPrefix** rimuove un prefisso IP pubblico di Azure purché non siano stati assegnati indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="c64f1-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="c64f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c64f1-110">EXAMPLES</span></span>

### <span data-ttu-id="c64f1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c64f1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="c64f1-112">Rimuove il prefisso IP pubblico con il nome $prefixName dal gruppo di risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="c64f1-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="c64f1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c64f1-113">PARAMETERS</span></span>

### <span data-ttu-id="c64f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c64f1-114">-AsJob</span></span>
<span data-ttu-id="c64f1-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c64f1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c64f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64f1-116">-DefaultProfile</span></span>
<span data-ttu-id="c64f1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c64f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c64f1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c64f1-118">-Force</span></span>
<span data-ttu-id="c64f1-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c64f1-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c64f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c64f1-120">-InputObject</span></span>
<span data-ttu-id="c64f1-121">Un oggetto PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c64f1-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="c64f1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c64f1-122">-Name</span></span>
<span data-ttu-id="c64f1-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c64f1-123">The resource name.</span></span>

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

### <span data-ttu-id="c64f1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c64f1-124">-PassThru</span></span>
<span data-ttu-id="c64f1-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c64f1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c64f1-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c64f1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c64f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="c64f1-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c64f1-128">The resource group name.</span></span>

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

### <span data-ttu-id="c64f1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c64f1-129">-ResourceId</span></span>
<span data-ttu-id="c64f1-130">ResourceId per la risorsa da rimuovere</span><span class="sxs-lookup"><span data-stu-id="c64f1-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="c64f1-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c64f1-131">-Confirm</span></span>
<span data-ttu-id="c64f1-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c64f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c64f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c64f1-133">-WhatIf</span></span>
<span data-ttu-id="c64f1-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c64f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c64f1-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c64f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c64f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64f1-136">CommonParameters</span></span>
<span data-ttu-id="c64f1-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c64f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64f1-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64f1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64f1-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c64f1-139">INPUTS</span></span>

### <span data-ttu-id="c64f1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c64f1-140">System.String</span></span>

### <span data-ttu-id="c64f1-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c64f1-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="c64f1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c64f1-142">OUTPUTS</span></span>

### <span data-ttu-id="c64f1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c64f1-143">System.Boolean</span></span>

## <span data-ttu-id="c64f1-144">Note</span><span class="sxs-lookup"><span data-stu-id="c64f1-144">NOTES</span></span>

## <span data-ttu-id="c64f1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c64f1-145">RELATED LINKS</span></span>

[<span data-ttu-id="c64f1-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c64f1-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="c64f1-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c64f1-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="c64f1-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c64f1-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
