---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: d908f99e9a1eaa191b45ed08cdb69ebf40b21756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685534"
---
# <span data-ttu-id="74cf2-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cf2-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="74cf2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="74cf2-103">Crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="74cf2-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74cf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74cf2-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74cf2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="74cf2-106">Il cmdlet **New-AzureRmContainerService** crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="74cf2-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="74cf2-107">Specifica un oggetto servizio contenitore che puoi creare usando il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="74cf2-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="74cf2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74cf2-108">EXAMPLES</span></span>

### <span data-ttu-id="74cf2-109">Esempio 1: creare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="74cf2-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="74cf2-110">Il primo comando crea un gruppo di risorse denominato ResourceGroup17 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="74cf2-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="74cf2-111">Per altre informazioni, vedere il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="74cf2-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="74cf2-112">Il secondo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="74cf2-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="74cf2-113">Per altre informazioni, vedere il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="74cf2-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="74cf2-114">Il comando finale crea un servizio contenitore per il contenitore archiviato in $Container.</span><span class="sxs-lookup"><span data-stu-id="74cf2-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="74cf2-115">Il servizio è denominato csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="74cf2-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="74cf2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74cf2-116">PARAMETERS</span></span>

### <span data-ttu-id="74cf2-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="74cf2-117">-ContainerService</span></span>
<span data-ttu-id="74cf2-118">Specifica un oggetto servizio contenitore che contiene le proprietà per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="74cf2-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="74cf2-119">Per ottenere un oggetto **ContainerService** , usa il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="74cf2-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="74cf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cf2-120">-DefaultProfile</span></span>
<span data-ttu-id="74cf2-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74cf2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74cf2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="74cf2-122">-Name</span></span>
<span data-ttu-id="74cf2-123">Specifica il nome del servizio contenitore creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74cf2-123">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="74cf2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74cf2-124">-ResourceGroupName</span></span>
<span data-ttu-id="74cf2-125">Specifica il gruppo di risorse in cui questo cmdlet distribuisce il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="74cf2-125">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="74cf2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74cf2-126">-Confirm</span></span>
<span data-ttu-id="74cf2-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74cf2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74cf2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74cf2-128">-WhatIf</span></span>
<span data-ttu-id="74cf2-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74cf2-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="74cf2-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74cf2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74cf2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cf2-131">CommonParameters</span></span>
<span data-ttu-id="74cf2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74cf2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cf2-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74cf2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cf2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74cf2-134">INPUTS</span></span>

## <span data-ttu-id="74cf2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74cf2-135">OUTPUTS</span></span>

## <span data-ttu-id="74cf2-136">Note</span><span class="sxs-lookup"><span data-stu-id="74cf2-136">NOTES</span></span>

## <span data-ttu-id="74cf2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74cf2-137">RELATED LINKS</span></span>

[<span data-ttu-id="74cf2-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cf2-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="74cf2-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="74cf2-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="74cf2-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cf2-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="74cf2-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="74cf2-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


