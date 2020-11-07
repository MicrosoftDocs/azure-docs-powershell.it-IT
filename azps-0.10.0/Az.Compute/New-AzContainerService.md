---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: b8f453200f2365272461373214ec92580212c4b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863666"
---
# <span data-ttu-id="8396f-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-101">New-AzContainerService</span></span>

## <span data-ttu-id="8396f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8396f-102">SYNOPSIS</span></span>
<span data-ttu-id="8396f-103">Crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="8396f-103">Creates a container service.</span></span>

## <span data-ttu-id="8396f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8396f-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8396f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8396f-105">DESCRIPTION</span></span>
<span data-ttu-id="8396f-106">Il cmdlet **New-AzContainerService** crea un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="8396f-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="8396f-107">Specifica un oggetto servizio contenitore che puoi creare usando il cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="8396f-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="8396f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8396f-108">EXAMPLES</span></span>

### <span data-ttu-id="8396f-109">Esempio 1: creare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="8396f-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="8396f-110">Il primo comando crea un gruppo di risorse denominato ResourceGroup17 nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="8396f-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="8396f-111">Per altre informazioni, vedere il cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8396f-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="8396f-112">Il secondo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="8396f-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8396f-113">Per altre informazioni, vedere il cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="8396f-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="8396f-114">Il comando finale crea un servizio contenitore per il contenitore archiviato in $Container.</span><span class="sxs-lookup"><span data-stu-id="8396f-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="8396f-115">Il servizio è denominato csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="8396f-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="8396f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8396f-116">PARAMETERS</span></span>

### <span data-ttu-id="8396f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8396f-117">-AsJob</span></span>
<span data-ttu-id="8396f-118">RRun cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="8396f-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8396f-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-119">-ContainerService</span></span>
<span data-ttu-id="8396f-120">Specifica un oggetto servizio contenitore che contiene le proprietà per il nuovo servizio.</span><span class="sxs-lookup"><span data-stu-id="8396f-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="8396f-121">Per ottenere un oggetto **ContainerService** , usa il cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="8396f-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="8396f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8396f-122">-DefaultProfile</span></span>
<span data-ttu-id="8396f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8396f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8396f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8396f-124">-Name</span></span>
<span data-ttu-id="8396f-125">Specifica il nome del servizio contenitore creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8396f-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8396f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8396f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8396f-127">Specifica il gruppo di risorse in cui questo cmdlet distribuisce il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="8396f-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="8396f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8396f-128">-Confirm</span></span>
<span data-ttu-id="8396f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8396f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8396f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8396f-130">-WhatIf</span></span>
<span data-ttu-id="8396f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8396f-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8396f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8396f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8396f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8396f-133">CommonParameters</span></span>
<span data-ttu-id="8396f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8396f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8396f-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8396f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8396f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8396f-136">INPUTS</span></span>

### <span data-ttu-id="8396f-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-137">ContainerService</span></span>
<span data-ttu-id="8396f-138">Il parametro ' ContainerService ' accetta il valore di tipo ' ContainerService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8396f-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="8396f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8396f-139">OUTPUTS</span></span>

### <span data-ttu-id="8396f-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="8396f-141">Note</span><span class="sxs-lookup"><span data-stu-id="8396f-141">NOTES</span></span>

## <span data-ttu-id="8396f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8396f-142">RELATED LINKS</span></span>

[<span data-ttu-id="8396f-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="8396f-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8396f-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="8396f-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="8396f-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8396f-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


