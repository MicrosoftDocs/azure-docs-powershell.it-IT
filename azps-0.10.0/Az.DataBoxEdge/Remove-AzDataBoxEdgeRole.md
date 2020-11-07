---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9120a07ed1483c433429621bef1e21d4bb4ecaa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863190"
---
# <span data-ttu-id="cf1f6-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cf1f6-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="cf1f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1f6-103">Rimuove il ruolo di sacco associato per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="cf1f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf1f6-104">SYNTAX</span></span>

### <span data-ttu-id="cf1f6-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf1f6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1f6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1f6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1f6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1f6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf1f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf1f6-108">DESCRIPTION</span></span>
<span data-ttu-id="cf1f6-109">Il cmdlet **Remove-AzDataBoxEdgeRole** consente di rimuovere il ruolo degli Stati associati per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="cf1f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf1f6-110">EXAMPLES</span></span>

### <span data-ttu-id="cf1f6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf1f6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="cf1f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf1f6-112">PARAMETERS</span></span>

### <span data-ttu-id="cf1f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf1f6-113">-AsJob</span></span>
<span data-ttu-id="cf1f6-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cf1f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf1f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1f6-115">-DefaultProfile</span></span>
<span data-ttu-id="cf1f6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf1f6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cf1f6-117">-DeviceName</span></span>
<span data-ttu-id="cf1f6-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="cf1f6-118">Device Name</span></span>

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

### <span data-ttu-id="cf1f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf1f6-119">-InputObject</span></span>
<span data-ttu-id="cf1f6-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="cf1f6-120">Input Object</span></span>

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

### <span data-ttu-id="cf1f6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf1f6-121">-Name</span></span>
<span data-ttu-id="cf1f6-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="cf1f6-122">Resource Name</span></span>

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

### <span data-ttu-id="cf1f6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf1f6-123">-PassThru</span></span>
<span data-ttu-id="cf1f6-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="cf1f6-124">returns true if successful</span></span>

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

### <span data-ttu-id="cf1f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf1f6-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cf1f6-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cf1f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1f6-127">-ResourceId</span></span>
<span data-ttu-id="cf1f6-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1f6-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="cf1f6-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf1f6-129">-Confirm</span></span>
<span data-ttu-id="cf1f6-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf1f6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf1f6-131">-WhatIf</span></span>
<span data-ttu-id="cf1f6-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf1f6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf1f6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1f6-134">CommonParameters</span></span>
<span data-ttu-id="cf1f6-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1f6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1f6-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf1f6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1f6-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf1f6-137">INPUTS</span></span>

### <span data-ttu-id="cf1f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cf1f6-138">System.String</span></span>

### <span data-ttu-id="cf1f6-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cf1f6-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="cf1f6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf1f6-140">OUTPUTS</span></span>

### <span data-ttu-id="cf1f6-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cf1f6-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="cf1f6-142">Note</span><span class="sxs-lookup"><span data-stu-id="cf1f6-142">NOTES</span></span>

## <span data-ttu-id="cf1f6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf1f6-143">RELATED LINKS</span></span>
