---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 1a15486b3e24dec3af66cb98391bd8322c28d2e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861602"
---
# <span data-ttu-id="7ff6d-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-101">Update-AzContainerService</span></span>

## <span data-ttu-id="7ff6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ff6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff6d-103">Aggiorna lo stato di un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="7ff6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ff6d-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ff6d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ff6d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff6d-106">Il cmdlet **Update-AzContainerService** aggiorna lo stato di un servizio contenitore in base a un'istanza locale del servizio.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="7ff6d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ff6d-107">EXAMPLES</span></span>

### <span data-ttu-id="7ff6d-108">Esempio 1: aggiornare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="7ff6d-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="7ff6d-109">Questo comando ottiene il servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="7ff6d-110">Il comando passa l'oggetto al cmdlet Remove-AzContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="7ff6d-111">**Remove-AzContainerServiceAgentPoolProfile** rimuove il profilo denominato AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="7ff6d-112">Il comando passa il risultato al cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="7ff6d-113">**Add-AzContainerServiceAgentPoolProfile** aggiunge un profilo con il nome AgentPool01 e ha le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="7ff6d-114">Il comando passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="7ff6d-115">Il cmdlet corrente aggiorna il servizio contenitore per riflettere le modifiche apportate in questo comando.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="7ff6d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ff6d-116">PARAMETERS</span></span>

### <span data-ttu-id="7ff6d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ff6d-117">-AsJob</span></span>
<span data-ttu-id="7ff6d-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7ff6d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ff6d-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-119">-ContainerService</span></span>
<span data-ttu-id="7ff6d-120">Specifica un oggetto **ContainerService** locale che contiene le modifiche.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ff6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff6d-121">-DefaultProfile</span></span>
<span data-ttu-id="7ff6d-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ff6d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ff6d-123">-Name</span></span>
<span data-ttu-id="7ff6d-124">Specifica il nome del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ff6d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff6d-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ff6d-126">Specifica il gruppo di risorse del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ff6d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ff6d-127">-Confirm</span></span>
<span data-ttu-id="7ff6d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff6d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff6d-129">-WhatIf</span></span>
<span data-ttu-id="7ff6d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7ff6d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff6d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff6d-132">CommonParameters</span></span>
<span data-ttu-id="7ff6d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff6d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff6d-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff6d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff6d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ff6d-135">INPUTS</span></span>

### <span data-ttu-id="7ff6d-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-136">ContainerService</span></span>
<span data-ttu-id="7ff6d-137">Il parametro ' ContainerService ' accetta il valore di tipo ' ContainerService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7ff6d-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="7ff6d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ff6d-138">OUTPUTS</span></span>

### <span data-ttu-id="7ff6d-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="7ff6d-140">Note</span><span class="sxs-lookup"><span data-stu-id="7ff6d-140">NOTES</span></span>

## <span data-ttu-id="7ff6d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ff6d-141">RELATED LINKS</span></span>

[<span data-ttu-id="7ff6d-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7ff6d-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="7ff6d-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="7ff6d-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="7ff6d-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7ff6d-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="7ff6d-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7ff6d-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


