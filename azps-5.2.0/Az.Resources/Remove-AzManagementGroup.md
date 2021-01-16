---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325539"
---
# <span data-ttu-id="a5aae-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5aae-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="a5aae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5aae-102">SYNOPSIS</span></span>
<span data-ttu-id="a5aae-103">Rimuove un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="a5aae-103">Removes a Management Group</span></span>

## <span data-ttu-id="a5aae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5aae-104">SYNTAX</span></span>

### <span data-ttu-id="a5aae-105">GroupOperations (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5aae-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5aae-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="a5aae-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5aae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5aae-107">DESCRIPTION</span></span>
<span data-ttu-id="a5aae-108">Il cmdlet **Remove-AzManagementGroup** Elimina un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="a5aae-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="a5aae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5aae-109">EXAMPLES</span></span>

### <span data-ttu-id="a5aae-110">Esempio 1: rimuovere un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="a5aae-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="a5aae-111">Esempio 2: rimuovere un gruppo di gestione eseguendo il piping di un oggetto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5aae-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="a5aae-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5aae-112">PARAMETERS</span></span>

### <span data-ttu-id="a5aae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5aae-113">-DefaultProfile</span></span>
<span data-ttu-id="a5aae-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5aae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5aae-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a5aae-115">-GroupName</span></span>
<span data-ttu-id="a5aae-116">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="a5aae-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5aae-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5aae-117">-InputObject</span></span>
<span data-ttu-id="a5aae-118">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="a5aae-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="a5aae-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5aae-119">-PassThru</span></span>
<span data-ttu-id="a5aae-120">Ritorno `true` all'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="a5aae-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="a5aae-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5aae-121">-Confirm</span></span>
<span data-ttu-id="a5aae-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5aae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5aae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5aae-123">-WhatIf</span></span>
<span data-ttu-id="a5aae-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5aae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5aae-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5aae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5aae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5aae-126">CommonParameters</span></span>
<span data-ttu-id="a5aae-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5aae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5aae-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5aae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5aae-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5aae-129">INPUTS</span></span>

### <span data-ttu-id="a5aae-130">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5aae-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="a5aae-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5aae-131">OUTPUTS</span></span>

### <span data-ttu-id="a5aae-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5aae-132">System.Boolean</span></span>

## <span data-ttu-id="a5aae-133">Note</span><span class="sxs-lookup"><span data-stu-id="a5aae-133">NOTES</span></span>

## <span data-ttu-id="a5aae-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5aae-134">RELATED LINKS</span></span>
