---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: bacc9366292225e07fd07ac65726018f1d1879e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509263"
---
# <span data-ttu-id="1519e-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="1519e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1519e-102">SYNOPSIS</span></span>
<span data-ttu-id="1519e-103">Aggiorna lo stato di un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="1519e-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1519e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1519e-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1519e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1519e-105">DESCRIPTION</span></span>
<span data-ttu-id="1519e-106">Il cmdlet **Update-AzureRmContainerService** aggiorna lo stato di un servizio contenitore in base a un'istanza locale del servizio.</span><span class="sxs-lookup"><span data-stu-id="1519e-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="1519e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1519e-107">EXAMPLES</span></span>

### <span data-ttu-id="1519e-108">Esempio 1: aggiornare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="1519e-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="1519e-109">Questo comando ottiene il servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="1519e-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="1519e-110">Il comando passa l'oggetto al cmdlet Remove-AzureRmContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1519e-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1519e-111">**Remove-AzureRmContainerServiceAgentPoolProfile** rimuove il profilo denominato AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="1519e-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="1519e-112">Il comando passa il risultato al cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="1519e-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="1519e-113">**Add-AzureRmContainerServiceAgentPoolProfile** aggiunge un profilo con il nome AgentPool01 e ha le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="1519e-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="1519e-114">Il comando passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="1519e-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="1519e-115">Il cmdlet corrente aggiorna il servizio contenitore per riflettere le modifiche apportate in questo comando.</span><span class="sxs-lookup"><span data-stu-id="1519e-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="1519e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1519e-116">PARAMETERS</span></span>

### <span data-ttu-id="1519e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1519e-117">-AsJob</span></span>
<span data-ttu-id="1519e-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1519e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1519e-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-119">-ContainerService</span></span>
<span data-ttu-id="1519e-120">Specifica un oggetto **ContainerService** locale che contiene le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1519e-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1519e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1519e-121">-DefaultProfile</span></span>
<span data-ttu-id="1519e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1519e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1519e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1519e-123">-Name</span></span>
<span data-ttu-id="1519e-124">Specifica il nome del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="1519e-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1519e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1519e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1519e-126">Specifica il gruppo di risorse del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="1519e-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1519e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1519e-127">-Confirm</span></span>
<span data-ttu-id="1519e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1519e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1519e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1519e-129">-WhatIf</span></span>
<span data-ttu-id="1519e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1519e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1519e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1519e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1519e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1519e-132">CommonParameters</span></span>
<span data-ttu-id="1519e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1519e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1519e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1519e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1519e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1519e-135">INPUTS</span></span>

### <span data-ttu-id="1519e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1519e-136">System.String</span></span>

### <span data-ttu-id="1519e-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="1519e-138">Parametri: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1519e-138">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="1519e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1519e-139">OUTPUTS</span></span>

### <span data-ttu-id="1519e-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1519e-141">Note</span><span class="sxs-lookup"><span data-stu-id="1519e-141">NOTES</span></span>

## <span data-ttu-id="1519e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1519e-142">RELATED LINKS</span></span>

[<span data-ttu-id="1519e-143">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1519e-143">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="1519e-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="1519e-145">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-145">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="1519e-146">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1519e-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="1519e-147">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1519e-147">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


