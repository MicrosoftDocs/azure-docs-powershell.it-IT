---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520149"
---
# <span data-ttu-id="f6d87-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f6d87-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="f6d87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6d87-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d87-103">Rimuove un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="f6d87-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6d87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6d87-104">SYNTAX</span></span>

### <span data-ttu-id="f6d87-105">GroupOperations (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6d87-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6d87-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="f6d87-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6d87-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6d87-107">DESCRIPTION</span></span>
<span data-ttu-id="f6d87-108">Il cmdlet **Remove-AzureRmManagementGroup** Elimina un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="f6d87-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="f6d87-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6d87-109">EXAMPLES</span></span>

### <span data-ttu-id="f6d87-110">Esempio 1-rimuovere un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="f6d87-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="f6d87-111">Esempio 2-rimuovere un gruppo di gestione eseguendo il piping di un oggetto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f6d87-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="f6d87-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6d87-112">PARAMETERS</span></span>

### <span data-ttu-id="f6d87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d87-113">-DefaultProfile</span></span>
<span data-ttu-id="f6d87-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d87-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f6d87-115">-GroupName</span></span>
<span data-ttu-id="f6d87-116">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="f6d87-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6d87-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6d87-117">-InputObject</span></span>
<span data-ttu-id="f6d87-118">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="f6d87-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d87-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6d87-119">-PassThru</span></span>
<span data-ttu-id="f6d87-120">Ritorno `true` all'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="f6d87-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f6d87-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6d87-121">-Confirm</span></span>
<span data-ttu-id="f6d87-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6d87-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6d87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6d87-123">-WhatIf</span></span>
<span data-ttu-id="f6d87-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6d87-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6d87-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6d87-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6d87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d87-126">CommonParameters</span></span>
<span data-ttu-id="f6d87-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d87-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d87-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d87-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6d87-129">INPUTS</span></span>

### <span data-ttu-id="f6d87-130">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f6d87-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="f6d87-131">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f6d87-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f6d87-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6d87-132">OUTPUTS</span></span>

### <span data-ttu-id="f6d87-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6d87-133">System.Boolean</span></span>

## <span data-ttu-id="f6d87-134">Note</span><span class="sxs-lookup"><span data-stu-id="f6d87-134">NOTES</span></span>

## <span data-ttu-id="f6d87-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6d87-135">RELATED LINKS</span></span>
