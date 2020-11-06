---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: ff337ae0f5d0da86b035905bf83d2719edf1f4f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508360"
---
# <span data-ttu-id="6b7e3-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b7e3-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="6b7e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7e3-103">Crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b7e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b7e3-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b7e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b7e3-105">DESCRIPTION</span></span>
<span data-ttu-id="6b7e3-106">Il cmdlet **New-AzureRmContainerService** crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="6b7e3-107">Specifica un oggetto servizio contenitore che puoi creare usando il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="6b7e3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b7e3-108">EXAMPLES</span></span>

### <span data-ttu-id="6b7e3-109">Esempio 1: creare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="6b7e3-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="6b7e3-110">Il primo comando crea un gruppo di risorse denominato ResourceGroup17 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="6b7e3-111">Per altre informazioni, vedere il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="6b7e3-112">Il secondo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6b7e3-113">Per altre informazioni, vedere il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="6b7e3-114">Il comando finale crea un servizio contenitore per il contenitore archiviato in $Container.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="6b7e3-115">Il servizio è denominato csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="6b7e3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b7e3-116">PARAMETERS</span></span>

### <span data-ttu-id="6b7e3-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="6b7e3-117">-ContainerService</span></span>
<span data-ttu-id="6b7e3-118">Specifica un oggetto servizio contenitore che contiene le proprietà per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="6b7e3-119">Per ottenere un oggetto **ContainerService** , usa il cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b7e3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b7e3-120">-Name</span></span>
<span data-ttu-id="6b7e3-121">Specifica il nome del servizio contenitore creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-121">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6b7e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b7e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b7e3-123">Specifica il gruppo di risorse in cui questo cmdlet distribuisce il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-123">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="6b7e3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b7e3-124">-Confirm</span></span>
<span data-ttu-id="6b7e3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b7e3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b7e3-126">-WhatIf</span></span>
<span data-ttu-id="6b7e3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-127">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6b7e3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b7e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7e3-129">CommonParameters</span></span>
<span data-ttu-id="6b7e3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7e3-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b7e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7e3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b7e3-132">INPUTS</span></span>

### <span data-ttu-id="6b7e3-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6b7e3-133">None</span></span>
<span data-ttu-id="6b7e3-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6b7e3-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b7e3-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b7e3-135">OUTPUTS</span></span>

## <span data-ttu-id="6b7e3-136">Note</span><span class="sxs-lookup"><span data-stu-id="6b7e3-136">NOTES</span></span>

## <span data-ttu-id="6b7e3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b7e3-137">RELATED LINKS</span></span>

[<span data-ttu-id="6b7e3-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b7e3-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="6b7e3-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6b7e3-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="6b7e3-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b7e3-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="6b7e3-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b7e3-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


