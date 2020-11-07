---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686206"
---
# <span data-ttu-id="67bd5-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="67bd5-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="67bd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="67bd5-103">Crea una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67bd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67bd5-104">SYNTAX</span></span>

### <span data-ttu-id="67bd5-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67bd5-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67bd5-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67bd5-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67bd5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67bd5-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67bd5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67bd5-108">DESCRIPTION</span></span>
<span data-ttu-id="67bd5-109">Il cmdlet New-AzureRmContainerRegistryReplication crea una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="67bd5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67bd5-110">EXAMPLES</span></span>

### <span data-ttu-id="67bd5-111">Esempio 1: creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="67bd5-112">Creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="67bd5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67bd5-113">PARAMETERS</span></span>

### <span data-ttu-id="67bd5-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67bd5-114">-Confirm</span></span>
<span data-ttu-id="67bd5-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67bd5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67bd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67bd5-116">-DefaultProfile</span></span>
<span data-ttu-id="67bd5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67bd5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67bd5-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="67bd5-118">-Location</span></span>
<span data-ttu-id="67bd5-119">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-119">Container Registry Location.</span></span>
<span data-ttu-id="67bd5-120">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67bd5-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67bd5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="67bd5-121">-Name</span></span>
<span data-ttu-id="67bd5-122">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="67bd5-123">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="67bd5-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67bd5-124">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="67bd5-124">-Registry</span></span>
<span data-ttu-id="67bd5-125">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67bd5-126">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="67bd5-126">-RegistryName</span></span>
<span data-ttu-id="67bd5-127">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67bd5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67bd5-128">-ResourceGroupName</span></span>
<span data-ttu-id="67bd5-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67bd5-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67bd5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67bd5-130">-ResourceId</span></span>
<span data-ttu-id="67bd5-131">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="67bd5-131">The container registry resource id</span></span>

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

### <span data-ttu-id="67bd5-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="67bd5-132">-Tag</span></span>
<span data-ttu-id="67bd5-133">Tag del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="67bd5-133">Container Registry Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67bd5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67bd5-134">-WhatIf</span></span>
<span data-ttu-id="67bd5-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67bd5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67bd5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67bd5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67bd5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67bd5-137">CommonParameters</span></span>
<span data-ttu-id="67bd5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67bd5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67bd5-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67bd5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67bd5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67bd5-140">INPUTS</span></span>

### <span data-ttu-id="67bd5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="67bd5-141">System.String</span></span>

## <span data-ttu-id="67bd5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67bd5-142">OUTPUTS</span></span>

### <span data-ttu-id="67bd5-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="67bd5-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="67bd5-144">Note</span><span class="sxs-lookup"><span data-stu-id="67bd5-144">NOTES</span></span>

## <span data-ttu-id="67bd5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67bd5-145">RELATED LINKS</span></span>

[<span data-ttu-id="67bd5-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="67bd5-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="67bd5-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="67bd5-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
