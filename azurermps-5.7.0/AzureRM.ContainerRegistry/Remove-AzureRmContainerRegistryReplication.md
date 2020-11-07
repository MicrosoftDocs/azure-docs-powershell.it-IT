---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686202"
---
# <span data-ttu-id="b4e75-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b4e75-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="b4e75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4e75-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e75-103">Rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4e75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4e75-104">SYNTAX</span></span>

### <span data-ttu-id="b4e75-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4e75-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e75-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4e75-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e75-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4e75-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e75-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4e75-108">DESCRIPTION</span></span>
<span data-ttu-id="b4e75-109">Il cmdlet Remove-AzureRmContainerRegistryReplication rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="b4e75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4e75-110">EXAMPLES</span></span>

### <span data-ttu-id="b4e75-111">Esempio 1: rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="b4e75-112">Rimuove una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="b4e75-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4e75-113">PARAMETERS</span></span>

### <span data-ttu-id="b4e75-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4e75-114">-Confirm</span></span>
<span data-ttu-id="b4e75-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4e75-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e75-116">-DefaultProfile</span></span>
<span data-ttu-id="b4e75-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e75-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4e75-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4e75-118">-Name</span></span>
<span data-ttu-id="b4e75-119">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="b4e75-120">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b4e75-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-121">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b4e75-121">-RegistryName</span></span>
<span data-ttu-id="b4e75-122">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="b4e75-123">-Replicatoin</span></span>
<span data-ttu-id="b4e75-124">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4e75-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e75-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4e75-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4e75-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e75-127">-ResourceId</span></span>
<span data-ttu-id="b4e75-128">ID risorsa di replica del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="b4e75-128">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e75-129">-WhatIf</span></span>
<span data-ttu-id="b4e75-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4e75-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e75-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4e75-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e75-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4e75-132">-PassThru</span></span>
<span data-ttu-id="b4e75-133">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b4e75-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b4e75-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e75-134">CommonParameters</span></span>
<span data-ttu-id="b4e75-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e75-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e75-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e75-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e75-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4e75-137">INPUTS</span></span>

### <span data-ttu-id="b4e75-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b4e75-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="b4e75-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e75-139">System.String</span></span>

## <span data-ttu-id="b4e75-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4e75-140">OUTPUTS</span></span>

### <span data-ttu-id="b4e75-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="b4e75-141">System.Object</span></span>

## <span data-ttu-id="b4e75-142">Note</span><span class="sxs-lookup"><span data-stu-id="b4e75-142">NOTES</span></span>

## <span data-ttu-id="b4e75-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4e75-143">RELATED LINKS</span></span>

[<span data-ttu-id="b4e75-144">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b4e75-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="b4e75-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b4e75-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

