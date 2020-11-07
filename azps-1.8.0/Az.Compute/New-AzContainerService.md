---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: cd988a78962e1603be42e867fbc27bd0e58ff69c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852077"
---
# <span data-ttu-id="2e05c-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-101">New-AzContainerService</span></span>

## <span data-ttu-id="2e05c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e05c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e05c-103">Crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="2e05c-103">Creates a container service.</span></span>

## <span data-ttu-id="2e05c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e05c-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e05c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e05c-105">DESCRIPTION</span></span>
<span data-ttu-id="2e05c-106">Il cmdlet **New-AzContainerService** crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="2e05c-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="2e05c-107">Specifica un oggetto servizio contenitore che puoi creare usando il cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="2e05c-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="2e05c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e05c-108">EXAMPLES</span></span>

### <span data-ttu-id="2e05c-109">Esempio 1: creare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="2e05c-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="2e05c-110">Il primo comando crea un gruppo di risorse denominato ResourceGroup17 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="2e05c-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="2e05c-111">Per altre informazioni, vedere il cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2e05c-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2e05c-112">Il secondo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="2e05c-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2e05c-113">Per altre informazioni, vedere il cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="2e05c-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="2e05c-114">Il comando finale crea un servizio contenitore per il contenitore archiviato in $Container.</span><span class="sxs-lookup"><span data-stu-id="2e05c-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="2e05c-115">Il servizio è denominato csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="2e05c-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="2e05c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e05c-116">PARAMETERS</span></span>

### <span data-ttu-id="2e05c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e05c-117">-AsJob</span></span>
<span data-ttu-id="2e05c-118">RRun cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2e05c-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2e05c-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-119">-ContainerService</span></span>
<span data-ttu-id="2e05c-120">Specifica un oggetto servizio contenitore che contiene le proprietà per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="2e05c-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="2e05c-121">Per ottenere un oggetto **ContainerService** , usa il cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="2e05c-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="2e05c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e05c-122">-DefaultProfile</span></span>
<span data-ttu-id="2e05c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e05c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e05c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e05c-124">-Name</span></span>
<span data-ttu-id="2e05c-125">Specifica il nome del servizio contenitore creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e05c-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2e05c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e05c-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e05c-127">Specifica il gruppo di risorse in cui questo cmdlet distribuisce il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="2e05c-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="2e05c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e05c-128">-Confirm</span></span>
<span data-ttu-id="2e05c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e05c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e05c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e05c-130">-WhatIf</span></span>
<span data-ttu-id="2e05c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e05c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e05c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e05c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e05c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e05c-133">CommonParameters</span></span>
<span data-ttu-id="2e05c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e05c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e05c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e05c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e05c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e05c-136">INPUTS</span></span>

### <span data-ttu-id="2e05c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2e05c-137">System.String</span></span>

### <span data-ttu-id="2e05c-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2e05c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e05c-139">OUTPUTS</span></span>

### <span data-ttu-id="2e05c-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2e05c-141">Note</span><span class="sxs-lookup"><span data-stu-id="2e05c-141">NOTES</span></span>

## <span data-ttu-id="2e05c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e05c-142">RELATED LINKS</span></span>

[<span data-ttu-id="2e05c-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="2e05c-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="2e05c-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="2e05c-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="2e05c-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="2e05c-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


