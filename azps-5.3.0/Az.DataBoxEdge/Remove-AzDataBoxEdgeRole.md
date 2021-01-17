---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477223"
---
# <span data-ttu-id="3ff87-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3ff87-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="3ff87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ff87-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff87-103">Rimuove il ruolo di sacco associato per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ff87-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="3ff87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ff87-104">SYNTAX</span></span>

### <span data-ttu-id="3ff87-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ff87-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff87-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff87-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff87-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff87-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff87-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff87-108">DESCRIPTION</span></span>
<span data-ttu-id="3ff87-109">Il cmdlet **Remove-AzDataBoxEdgeRole** consente di rimuovere il ruolo degli Stati associati per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="3ff87-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="3ff87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ff87-110">EXAMPLES</span></span>

### <span data-ttu-id="3ff87-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ff87-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="3ff87-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ff87-112">PARAMETERS</span></span>

### <span data-ttu-id="3ff87-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ff87-113">-AsJob</span></span>
<span data-ttu-id="3ff87-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3ff87-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ff87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff87-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff87-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff87-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3ff87-117">-DeviceName</span></span>
<span data-ttu-id="3ff87-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="3ff87-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff87-119">-InputObject</span></span>
<span data-ttu-id="3ff87-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="3ff87-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff87-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff87-121">-Name</span></span>
<span data-ttu-id="3ff87-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="3ff87-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff87-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ff87-123">-PassThru</span></span>
<span data-ttu-id="3ff87-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="3ff87-124">returns true if successful</span></span>

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

### <span data-ttu-id="3ff87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff87-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ff87-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3ff87-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff87-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff87-127">-ResourceId</span></span>
<span data-ttu-id="3ff87-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff87-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff87-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ff87-129">-Confirm</span></span>
<span data-ttu-id="3ff87-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff87-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff87-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff87-131">-WhatIf</span></span>
<span data-ttu-id="3ff87-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ff87-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ff87-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ff87-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff87-134">CommonParameters</span></span>
<span data-ttu-id="3ff87-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff87-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ff87-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff87-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ff87-137">INPUTS</span></span>

### <span data-ttu-id="3ff87-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff87-138">System.String</span></span>

### <span data-ttu-id="3ff87-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3ff87-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3ff87-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ff87-140">OUTPUTS</span></span>

### <span data-ttu-id="3ff87-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3ff87-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3ff87-142">Note</span><span class="sxs-lookup"><span data-stu-id="3ff87-142">NOTES</span></span>

## <span data-ttu-id="3ff87-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ff87-143">RELATED LINKS</span></span>
