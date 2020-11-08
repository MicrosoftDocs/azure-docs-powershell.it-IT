---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022549"
---
# <span data-ttu-id="23520-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-101">Update-AzContainerService</span></span>

## <span data-ttu-id="23520-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23520-102">SYNOPSIS</span></span>
<span data-ttu-id="23520-103">Aggiorna lo stato di un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="23520-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="23520-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23520-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23520-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23520-105">DESCRIPTION</span></span>
<span data-ttu-id="23520-106">Il cmdlet **Update-AzContainerService** aggiorna lo stato di un servizio contenitore in base a un'istanza locale del servizio.</span><span class="sxs-lookup"><span data-stu-id="23520-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="23520-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23520-107">EXAMPLES</span></span>

### <span data-ttu-id="23520-108">Esempio 1: aggiornare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="23520-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="23520-109">Questo comando ottiene il servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="23520-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="23520-110">Il comando passa l'oggetto al cmdlet Remove-AzContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="23520-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23520-111">**Remove-AzContainerServiceAgentPoolProfile** rimuove il profilo denominato AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="23520-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="23520-112">Il comando passa il risultato al cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="23520-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="23520-113">**Add-AzContainerServiceAgentPoolProfile** aggiunge un profilo con il nome AgentPool01 e ha le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="23520-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="23520-114">Il comando passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="23520-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="23520-115">Il cmdlet corrente aggiorna il servizio contenitore per riflettere le modifiche apportate in questo comando.</span><span class="sxs-lookup"><span data-stu-id="23520-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="23520-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23520-116">PARAMETERS</span></span>

### <span data-ttu-id="23520-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23520-117">-AsJob</span></span>
<span data-ttu-id="23520-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="23520-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23520-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-119">-ContainerService</span></span>
<span data-ttu-id="23520-120">Specifica un oggetto **ContainerService** locale che contiene le modifiche.</span><span class="sxs-lookup"><span data-stu-id="23520-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23520-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23520-121">-DefaultProfile</span></span>
<span data-ttu-id="23520-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23520-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23520-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="23520-123">-Name</span></span>
<span data-ttu-id="23520-124">Specifica il nome del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="23520-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23520-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23520-125">-ResourceGroupName</span></span>
<span data-ttu-id="23520-126">Specifica il gruppo di risorse del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="23520-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23520-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23520-127">-Confirm</span></span>
<span data-ttu-id="23520-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23520-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23520-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23520-129">-WhatIf</span></span>
<span data-ttu-id="23520-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23520-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23520-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23520-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23520-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23520-132">CommonParameters</span></span>
<span data-ttu-id="23520-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23520-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23520-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23520-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23520-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23520-135">INPUTS</span></span>

### <span data-ttu-id="23520-136">System. String</span><span class="sxs-lookup"><span data-stu-id="23520-136">System.String</span></span>

### <span data-ttu-id="23520-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="23520-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23520-138">OUTPUTS</span></span>

### <span data-ttu-id="23520-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="23520-140">Note</span><span class="sxs-lookup"><span data-stu-id="23520-140">NOTES</span></span>

## <span data-ttu-id="23520-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23520-141">RELATED LINKS</span></span>

[<span data-ttu-id="23520-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="23520-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="23520-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="23520-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="23520-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="23520-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="23520-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="23520-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


