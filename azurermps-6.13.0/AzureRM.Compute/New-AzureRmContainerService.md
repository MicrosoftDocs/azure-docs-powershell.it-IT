---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: 9dd2018fe6f84ff4657da799fbcba720e8523bde
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688678"
---
# <span data-ttu-id="c042d-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="c042d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c042d-102">SYNOPSIS</span></span>
<span data-ttu-id="c042d-103">Crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="c042d-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c042d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c042d-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c042d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c042d-105">DESCRIPTION</span></span>
<span data-ttu-id="c042d-106">Il cmdlet **New-AzureRmContainerService** crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="c042d-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="c042d-107">Specifica un oggetto servizio contenitore che puoi creare usando il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="c042d-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="c042d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c042d-108">EXAMPLES</span></span>

### <span data-ttu-id="c042d-109">Esempio 1: creare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="c042d-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="c042d-110">Il primo comando crea un gruppo di risorse denominato ResourceGroup17 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c042d-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="c042d-111">Per altre informazioni, vedere il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c042d-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="c042d-112">Il secondo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="c042d-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c042d-113">Per altre informazioni, vedere il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="c042d-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="c042d-114">Il comando finale crea un servizio contenitore per il contenitore archiviato in $Container.</span><span class="sxs-lookup"><span data-stu-id="c042d-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="c042d-115">Il servizio è denominato csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="c042d-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="c042d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c042d-116">PARAMETERS</span></span>

### <span data-ttu-id="c042d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c042d-117">-AsJob</span></span>
<span data-ttu-id="c042d-118">RRun cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="c042d-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c042d-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-119">-ContainerService</span></span>
<span data-ttu-id="c042d-120">Specifica un oggetto servizio contenitore che contiene le proprietà per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="c042d-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="c042d-121">Per ottenere un oggetto **ContainerService** , usa il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="c042d-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="c042d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c042d-122">-DefaultProfile</span></span>
<span data-ttu-id="c042d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c042d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c042d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c042d-124">-Name</span></span>
<span data-ttu-id="c042d-125">Specifica il nome del servizio contenitore creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c042d-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c042d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c042d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c042d-127">Specifica il gruppo di risorse in cui questo cmdlet distribuisce il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="c042d-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="c042d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c042d-128">-Confirm</span></span>
<span data-ttu-id="c042d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c042d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c042d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c042d-130">-WhatIf</span></span>
<span data-ttu-id="c042d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c042d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c042d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c042d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c042d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c042d-133">CommonParameters</span></span>
<span data-ttu-id="c042d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c042d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c042d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c042d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c042d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c042d-136">INPUTS</span></span>

### <span data-ttu-id="c042d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c042d-137">System.String</span></span>

### <span data-ttu-id="c042d-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="c042d-139">Parametri: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c042d-139">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="c042d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c042d-140">OUTPUTS</span></span>

### <span data-ttu-id="c042d-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="c042d-142">Note</span><span class="sxs-lookup"><span data-stu-id="c042d-142">NOTES</span></span>

## <span data-ttu-id="c042d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c042d-143">RELATED LINKS</span></span>

[<span data-ttu-id="c042d-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="c042d-145">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="c042d-145">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="c042d-146">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="c042d-147">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c042d-147">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


