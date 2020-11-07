---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 086085bd1a36c1508cf489d224ddd6bff4651c50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684668"
---
# <span data-ttu-id="07356-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-101">Update-AzContainerService</span></span>

## <span data-ttu-id="07356-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07356-102">SYNOPSIS</span></span>
<span data-ttu-id="07356-103">Aggiorna lo stato di un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="07356-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="07356-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07356-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07356-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07356-105">DESCRIPTION</span></span>
<span data-ttu-id="07356-106">Il cmdlet **Update-AzContainerService** aggiorna lo stato di un servizio contenitore in base a un'istanza locale del servizio.</span><span class="sxs-lookup"><span data-stu-id="07356-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="07356-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07356-107">EXAMPLES</span></span>

### <span data-ttu-id="07356-108">Esempio 1: aggiornare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="07356-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="07356-109">Questo comando ottiene il servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="07356-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="07356-110">Il comando passa l'oggetto al cmdlet Remove-AzContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="07356-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="07356-111">**Remove-AzContainerServiceAgentPoolProfile** rimuove il profilo denominato AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="07356-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="07356-112">Il comando passa il risultato al cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="07356-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="07356-113">**Add-AzContainerServiceAgentPoolProfile** aggiunge un profilo con il nome AgentPool01 e ha le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="07356-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="07356-114">Il comando passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="07356-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="07356-115">Il cmdlet corrente aggiorna il servizio contenitore per riflettere le modifiche apportate in questo comando.</span><span class="sxs-lookup"><span data-stu-id="07356-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="07356-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07356-116">PARAMETERS</span></span>

### <span data-ttu-id="07356-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07356-117">-AsJob</span></span>
<span data-ttu-id="07356-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07356-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07356-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-119">-ContainerService</span></span>
<span data-ttu-id="07356-120">Specifica un oggetto **ContainerService** locale che contiene le modifiche.</span><span class="sxs-lookup"><span data-stu-id="07356-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="07356-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07356-121">-DefaultProfile</span></span>
<span data-ttu-id="07356-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07356-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07356-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="07356-123">-Name</span></span>
<span data-ttu-id="07356-124">Specifica il nome del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="07356-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="07356-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07356-125">-ResourceGroupName</span></span>
<span data-ttu-id="07356-126">Specifica il gruppo di risorse del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="07356-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="07356-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07356-127">-Confirm</span></span>
<span data-ttu-id="07356-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07356-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07356-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07356-129">-WhatIf</span></span>
<span data-ttu-id="07356-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07356-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07356-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07356-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07356-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07356-132">CommonParameters</span></span>
<span data-ttu-id="07356-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07356-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07356-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07356-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07356-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07356-135">INPUTS</span></span>

### <span data-ttu-id="07356-136">System. String</span><span class="sxs-lookup"><span data-stu-id="07356-136">System.String</span></span>

### <span data-ttu-id="07356-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="07356-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07356-138">OUTPUTS</span></span>

### <span data-ttu-id="07356-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="07356-140">Note</span><span class="sxs-lookup"><span data-stu-id="07356-140">NOTES</span></span>

## <span data-ttu-id="07356-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07356-141">RELATED LINKS</span></span>

[<span data-ttu-id="07356-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="07356-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="07356-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="07356-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="07356-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="07356-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="07356-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="07356-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


