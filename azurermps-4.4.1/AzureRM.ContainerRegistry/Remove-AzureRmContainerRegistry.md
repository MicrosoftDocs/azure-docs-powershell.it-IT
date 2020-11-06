---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510747"
---
# <span data-ttu-id="de5ab-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de5ab-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="de5ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="de5ab-103">Rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de5ab-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de5ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de5ab-104">SYNTAX</span></span>

### <span data-ttu-id="de5ab-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de5ab-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5ab-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de5ab-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de5ab-107">DESCRIPTION</span></span>
<span data-ttu-id="de5ab-108">Il cmdlet **Remove-AzureRmContainerRegistry** rimuove un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de5ab-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="de5ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de5ab-109">EXAMPLES</span></span>

### <span data-ttu-id="de5ab-110">Esempio 1: rimuovere un registro di sistema contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="de5ab-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="de5ab-111">Questo comando rimuove il registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="de5ab-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="de5ab-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de5ab-112">PARAMETERS</span></span>

### <span data-ttu-id="de5ab-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="de5ab-113">-Name</span></span>
<span data-ttu-id="de5ab-114">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de5ab-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="de5ab-115">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="de5ab-115">-Registry</span></span>
<span data-ttu-id="de5ab-116">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="de5ab-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de5ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="de5ab-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de5ab-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="de5ab-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de5ab-119">-Confirm</span></span>
<span data-ttu-id="de5ab-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de5ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5ab-121">-WhatIf</span></span>
<span data-ttu-id="de5ab-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de5ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de5ab-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de5ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5ab-124">-DefaultProfile</span></span>
<span data-ttu-id="de5ab-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de5ab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de5ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5ab-126">CommonParameters</span></span>
<span data-ttu-id="de5ab-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5ab-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5ab-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de5ab-129">INPUTS</span></span>

### <span data-ttu-id="de5ab-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de5ab-130">PSContainerRegistry</span></span>
<span data-ttu-id="de5ab-131">Il parametro ' Registry ' accetta il valore di tipo ' PSContainerRegistry ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="de5ab-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="de5ab-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de5ab-132">OUTPUTS</span></span>

### <span data-ttu-id="de5ab-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de5ab-133">None</span></span>

## <span data-ttu-id="de5ab-134">Note</span><span class="sxs-lookup"><span data-stu-id="de5ab-134">NOTES</span></span>

## <span data-ttu-id="de5ab-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de5ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="de5ab-136">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de5ab-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="de5ab-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de5ab-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="de5ab-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de5ab-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

