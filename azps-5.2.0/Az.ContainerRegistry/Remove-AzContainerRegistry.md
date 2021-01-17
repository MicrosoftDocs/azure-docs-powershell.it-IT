---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356260"
---
# <span data-ttu-id="86ce5-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86ce5-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="86ce5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="86ce5-103">Rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="86ce5-103">Removes a container registry.</span></span>

## <span data-ttu-id="86ce5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86ce5-104">SYNTAX</span></span>

### <span data-ttu-id="86ce5-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86ce5-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ce5-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ce5-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ce5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ce5-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ce5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86ce5-108">DESCRIPTION</span></span>
<span data-ttu-id="86ce5-109">Il cmdlet Remove-AzContainerRegistry rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="86ce5-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="86ce5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86ce5-110">EXAMPLES</span></span>

### <span data-ttu-id="86ce5-111">Esempio 1: rimuovere un registro di sistema contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="86ce5-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="86ce5-112">Questo comando rimuove il registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="86ce5-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="86ce5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86ce5-113">PARAMETERS</span></span>

### <span data-ttu-id="86ce5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ce5-114">-DefaultProfile</span></span>
<span data-ttu-id="86ce5-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="86ce5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86ce5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="86ce5-116">-Name</span></span>
<span data-ttu-id="86ce5-117">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="86ce5-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="86ce5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86ce5-118">-PassThru</span></span>
<span data-ttu-id="86ce5-119">Indica che questo cmdlet restituisce true se la rimozione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="86ce5-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="86ce5-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="86ce5-120">-Registry</span></span>
<span data-ttu-id="86ce5-121">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="86ce5-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="86ce5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ce5-122">-ResourceGroupName</span></span>
<span data-ttu-id="86ce5-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86ce5-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="86ce5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86ce5-124">-ResourceId</span></span>
<span data-ttu-id="86ce5-125">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="86ce5-125">The container registry resource id</span></span>

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

### <span data-ttu-id="86ce5-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86ce5-126">-Confirm</span></span>
<span data-ttu-id="86ce5-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86ce5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ce5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ce5-128">-WhatIf</span></span>
<span data-ttu-id="86ce5-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86ce5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ce5-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86ce5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ce5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ce5-131">CommonParameters</span></span>
<span data-ttu-id="86ce5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ce5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ce5-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86ce5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ce5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86ce5-134">INPUTS</span></span>

### <span data-ttu-id="86ce5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="86ce5-135">System.String</span></span>

## <span data-ttu-id="86ce5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86ce5-136">OUTPUTS</span></span>

### <span data-ttu-id="86ce5-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86ce5-137">System.Boolean</span></span>

## <span data-ttu-id="86ce5-138">Note</span><span class="sxs-lookup"><span data-stu-id="86ce5-138">NOTES</span></span>

## <span data-ttu-id="86ce5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86ce5-139">RELATED LINKS</span></span>

[<span data-ttu-id="86ce5-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86ce5-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="86ce5-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86ce5-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="86ce5-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86ce5-142">Update-AzContainerRegistry</span></span>]()

