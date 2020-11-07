---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687337"
---
# <span data-ttu-id="b380f-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b380f-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="b380f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b380f-102">SYNOPSIS</span></span>
<span data-ttu-id="b380f-103">Rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b380f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b380f-104">SYNTAX</span></span>

### <span data-ttu-id="b380f-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b380f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b380f-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b380f-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b380f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b380f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b380f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b380f-108">DESCRIPTION</span></span>
<span data-ttu-id="b380f-109">Il cmdlet Remove-AzureRmContainerRegistryReplication rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="b380f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b380f-110">EXAMPLES</span></span>

### <span data-ttu-id="b380f-111">Esempio 1: rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="b380f-112">Rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="b380f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b380f-113">PARAMETERS</span></span>

### <span data-ttu-id="b380f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b380f-114">-DefaultProfile</span></span>
<span data-ttu-id="b380f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b380f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b380f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b380f-116">-Name</span></span>
<span data-ttu-id="b380f-117">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="b380f-118">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b380f-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b380f-119">-PassThru</span></span>
<span data-ttu-id="b380f-120">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b380f-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b380f-121">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b380f-121">-RegistryName</span></span>
<span data-ttu-id="b380f-122">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="b380f-123">-Replicatoin</span></span>
<span data-ttu-id="b380f-124">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b380f-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b380f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b380f-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b380f-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b380f-127">-ResourceId</span></span>
<span data-ttu-id="b380f-128">ID risorsa di replica del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="b380f-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b380f-129">-Confirm</span></span>
<span data-ttu-id="b380f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b380f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b380f-131">-WhatIf</span></span>
<span data-ttu-id="b380f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b380f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b380f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b380f-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b380f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b380f-134">CommonParameters</span></span>
<span data-ttu-id="b380f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b380f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b380f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b380f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b380f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b380f-137">INPUTS</span></span>

### <span data-ttu-id="b380f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b380f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="b380f-139">Parametri: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b380f-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="b380f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b380f-140">System.String</span></span>

## <span data-ttu-id="b380f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b380f-141">OUTPUTS</span></span>

### <span data-ttu-id="b380f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b380f-142">System.Boolean</span></span>

## <span data-ttu-id="b380f-143">Note</span><span class="sxs-lookup"><span data-stu-id="b380f-143">NOTES</span></span>

## <span data-ttu-id="b380f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b380f-144">RELATED LINKS</span></span>

[<span data-ttu-id="b380f-145">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b380f-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="b380f-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b380f-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

