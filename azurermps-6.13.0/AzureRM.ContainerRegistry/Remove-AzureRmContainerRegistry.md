---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687338"
---
# <span data-ttu-id="6d85e-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6d85e-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="6d85e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d85e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d85e-103">Rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="6d85e-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d85e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d85e-104">SYNTAX</span></span>

### <span data-ttu-id="6d85e-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d85e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d85e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d85e-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d85e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d85e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d85e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d85e-108">DESCRIPTION</span></span>
<span data-ttu-id="6d85e-109">Il cmdlet Remove-AzureRmContainerRegistry rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="6d85e-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="6d85e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d85e-110">EXAMPLES</span></span>

### <span data-ttu-id="6d85e-111">Esempio 1: rimuovere un registro di sistema contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="6d85e-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="6d85e-112">Questo comando rimuove il registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="6d85e-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="6d85e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d85e-113">PARAMETERS</span></span>

### <span data-ttu-id="6d85e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d85e-114">-DefaultProfile</span></span>
<span data-ttu-id="6d85e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6d85e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d85e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d85e-116">-Name</span></span>
<span data-ttu-id="6d85e-117">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="6d85e-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d85e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d85e-118">-PassThru</span></span>
<span data-ttu-id="6d85e-119">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="6d85e-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="6d85e-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="6d85e-120">-Registry</span></span>
<span data-ttu-id="6d85e-121">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="6d85e-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d85e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d85e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d85e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d85e-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d85e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d85e-124">-ResourceId</span></span>
<span data-ttu-id="6d85e-125">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="6d85e-125">The container registry resource id</span></span>

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

### <span data-ttu-id="6d85e-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d85e-126">-Confirm</span></span>
<span data-ttu-id="6d85e-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d85e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d85e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d85e-128">-WhatIf</span></span>
<span data-ttu-id="6d85e-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d85e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d85e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d85e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d85e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d85e-131">CommonParameters</span></span>
<span data-ttu-id="6d85e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d85e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d85e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d85e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d85e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d85e-134">INPUTS</span></span>

### <span data-ttu-id="6d85e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6d85e-135">System.String</span></span>

## <span data-ttu-id="6d85e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d85e-136">OUTPUTS</span></span>

### <span data-ttu-id="6d85e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d85e-137">System.Boolean</span></span>

## <span data-ttu-id="6d85e-138">Note</span><span class="sxs-lookup"><span data-stu-id="6d85e-138">NOTES</span></span>

## <span data-ttu-id="6d85e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d85e-139">RELATED LINKS</span></span>

[<span data-ttu-id="6d85e-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6d85e-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="6d85e-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6d85e-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="6d85e-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6d85e-142">Update-AzureRmContainerRegistry</span></span>]()

