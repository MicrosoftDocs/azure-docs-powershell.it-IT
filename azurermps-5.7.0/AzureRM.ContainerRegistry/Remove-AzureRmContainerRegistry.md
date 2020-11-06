---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516819"
---
# <span data-ttu-id="8de75-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8de75-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="8de75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8de75-102">SYNOPSIS</span></span>
<span data-ttu-id="8de75-103">Rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8de75-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8de75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8de75-104">SYNTAX</span></span>

### <span data-ttu-id="8de75-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8de75-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de75-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de75-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de75-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de75-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de75-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8de75-108">DESCRIPTION</span></span>
<span data-ttu-id="8de75-109">Il cmdlet Remove-AzureRmContainerRegistry rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8de75-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="8de75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8de75-110">EXAMPLES</span></span>

### <span data-ttu-id="8de75-111">Esempio 1: rimuovere un registro di sistema contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="8de75-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="8de75-112">Questo comando rimuove il registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="8de75-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="8de75-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8de75-113">PARAMETERS</span></span>

### <span data-ttu-id="8de75-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="8de75-114">-Name</span></span>
<span data-ttu-id="8de75-115">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8de75-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de75-116">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="8de75-116">-Registry</span></span>
<span data-ttu-id="8de75-117">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8de75-117">Container Registry Object.</span></span>

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

### <span data-ttu-id="8de75-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de75-118">-ResourceGroupName</span></span>
<span data-ttu-id="8de75-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8de75-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="8de75-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8de75-120">-Confirm</span></span>
<span data-ttu-id="8de75-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8de75-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de75-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de75-122">-WhatIf</span></span>
<span data-ttu-id="8de75-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8de75-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de75-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8de75-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de75-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de75-125">-DefaultProfile</span></span>
<span data-ttu-id="8de75-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8de75-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8de75-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8de75-127">-ResourceId</span></span>
<span data-ttu-id="8de75-128">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="8de75-128">The container registry resource id</span></span>

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

### <span data-ttu-id="8de75-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de75-129">-PassThru</span></span>
<span data-ttu-id="8de75-130">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="8de75-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8de75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de75-131">CommonParameters</span></span>
<span data-ttu-id="8de75-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de75-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de75-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de75-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8de75-134">INPUTS</span></span>

### <span data-ttu-id="8de75-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8de75-135">PSContainerRegistry</span></span>
<span data-ttu-id="8de75-136">Il parametro ' Registry ' accetta il valore di tipo ' PSContainerRegistry ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8de75-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="8de75-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8de75-137">OUTPUTS</span></span>

### <span data-ttu-id="8de75-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8de75-138">None</span></span>

## <span data-ttu-id="8de75-139">Note</span><span class="sxs-lookup"><span data-stu-id="8de75-139">NOTES</span></span>

## <span data-ttu-id="8de75-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8de75-140">RELATED LINKS</span></span>

[<span data-ttu-id="8de75-141">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8de75-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="8de75-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8de75-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="8de75-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8de75-143">Update-AzureRmContainerRegistry</span></span>]()

