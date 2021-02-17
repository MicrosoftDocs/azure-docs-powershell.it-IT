---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209954"
---
# <span data-ttu-id="ecfdb-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-101">Update-AzContainerService</span></span>

## <span data-ttu-id="ecfdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecfdb-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfdb-103">Aggiorna lo stato di un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="ecfdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecfdb-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfdb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecfdb-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfdb-106">Il cmdlet **Update-AzContainerService** aggiorna lo stato di un servizio contenitore in modo che corrisponda a un'istanza locale del servizio.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="ecfdb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecfdb-107">EXAMPLES</span></span>

### <span data-ttu-id="ecfdb-108">Esempio 1: Aggiornare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="ecfdb-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="ecfdb-109">Questo comando recupera il servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzContainerService contenitore.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="ecfdb-110">Il comando passa l'oggetto al cmdlet Remove-AzContainerServiceAgentPoolProfile tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ecfdb-111">**Remove-AzContainerServiceAgentPoolProfile** rimuove il profilo denominato AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="ecfdb-112">Il comando passa il risultato al cmdlet Add-AzContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="ecfdb-113">**Add-AzContainerServiceAgentPoolProfile** aggiunge un profilo con il nome AgentPool01 e con le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="ecfdb-114">Il comando passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="ecfdb-115">Il cmdlet corrente aggiorna il servizio contenitore per riflettere le modifiche apportate in questo comando.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="ecfdb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecfdb-116">PARAMETERS</span></span>

### <span data-ttu-id="ecfdb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecfdb-117">-AsJob</span></span>
<span data-ttu-id="ecfdb-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ecfdb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecfdb-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-119">-ContainerService</span></span>
<span data-ttu-id="ecfdb-120">Specifica un oggetto **ContainerService locale** che contiene modifiche.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="ecfdb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfdb-121">-DefaultProfile</span></span>
<span data-ttu-id="ecfdb-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecfdb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ecfdb-123">-Name</span></span>
<span data-ttu-id="ecfdb-124">Specifica il nome del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="ecfdb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfdb-125">-ResourceGroupName</span></span>
<span data-ttu-id="ecfdb-126">Specifica il gruppo di risorse del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="ecfdb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecfdb-127">-Confirm</span></span>
<span data-ttu-id="ecfdb-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfdb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfdb-129">-WhatIf</span></span>
<span data-ttu-id="ecfdb-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecfdb-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfdb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfdb-132">CommonParameters</span></span>
<span data-ttu-id="ecfdb-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfdb-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecfdb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfdb-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecfdb-135">INPUTS</span></span>

### <span data-ttu-id="ecfdb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ecfdb-136">System.String</span></span>

### <span data-ttu-id="ecfdb-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ecfdb-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecfdb-138">OUTPUTS</span></span>

### <span data-ttu-id="ecfdb-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ecfdb-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecfdb-140">NOTES</span></span>

## <span data-ttu-id="ecfdb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecfdb-141">RELATED LINKS</span></span>

[<span data-ttu-id="ecfdb-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="ecfdb-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="ecfdb-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="ecfdb-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="ecfdb-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ecfdb-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="ecfdb-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="ecfdb-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


